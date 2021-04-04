---
title: บทช่วยสอน Regression Suite Automation Tool
description: หัวข้อนี้จะแสดงวิธีการใช้ Regression Suite Automation Tool (RSAT) ซึ่งจะอธิบายถึงคุณลักษณะต่างๆ และแสดงตัวอย่างที่ใช้การเขียนสคริปต์ขั้นสูง
author: robinarh
manager: AnnBe
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: b8866d43ea8b6b6bea34c01cbcbc9e3575081c4c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568391"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="3aff0-104">บทช่วยสอน Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="3aff0-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3aff0-105">ใช้เครื่องมือเบราว์เซอร์อินเทอร์เน็ตของคุณเพื่อดาวน์โหลดและบันทึกหน้านี้ในรูปแบบ pdf</span><span class="sxs-lookup"><span data-stu-id="3aff0-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="3aff0-106">บทช่วยสอนนี้จะแนะนำคุณลักษณะขั้นสูงบางอย่างของ Regression Suite Automation Tool (RSAT) รวมถึงการกำหนดการสาธิต และอธิบายถึงกลยุทธ์และประเด็นการเรียนรู้ที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="3aff0-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="3aff0-107">ลักษณะการทำงานที่โดดเด่นของ RSAT และตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="3aff0-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="3aff0-108">ตรวจสอบความถูกต้องของค่าฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3aff0-108">Validate a field value</span></span>

<span data-ttu-id="3aff0-109">RSAT ช่วยให้คุณสามารถรวมขั้นตอนการตรวจสอบความถูกต้องภายในกรณีการทดสอบของคุณ เพื่อตรวจสอบความถูกต้องของค่าที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="3aff0-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="3aff0-110">สำหรับข้อมูลเกี่ยวกับลักษณะการทำงานนี้ โปรดดูบทความ [ตรวจสอบความถูกต้องของค่าที่คาดไว้](rsat-validate-expected.md)</span><span class="sxs-lookup"><span data-stu-id="3aff0-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="3aff0-111">ตัวอย่างต่อไปนี้แสดงวิธีการที่คุณสามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าปริมาณคงคลังคงเหลือมากกว่า 0 (ศูนย์) หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3aff0-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="3aff0-112">ในข้อมูลสาธิตในบริษัท **USMF** ให้สร้างการบันทึกงานที่มีขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3aff0-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="3aff0-113">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="3aff0-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="3aff0-114">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="3aff0-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3aff0-115">ตัวอย่างเช่น ตัวกรองในค่าของ **1000** สำหรับฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="3aff0-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="3aff0-116">เลือก **ปริมาณสินค้าคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="3aff0-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="3aff0-117">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="3aff0-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3aff0-118">ตัวอย่างเช่น ตัวกรองในค่าของ **1** สำหรับฟิลด์ **ไซต์**</span><span class="sxs-lookup"><span data-stu-id="3aff0-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="3aff0-119">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3aff0-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="3aff0-120">ตรวจสอบความถูกต้องว่าค่าของฟิลด์ **ทั้งหมดที่พร้อมใช้งาน** คือ **411.0000000000000000**</span><span class="sxs-lookup"><span data-stu-id="3aff0-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="3aff0-121">บันทึกการบันทึกงานเป็น **การบันทึกของนักพัฒนา** และแนบไปกับกรณีการทดสอบของคุณใน Azure Devops</span><span class="sxs-lookup"><span data-stu-id="3aff0-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="3aff0-122">เพิ่มกรณีการทดสอบไปยังแผนการทดสอบ และโหลดกรณีการทดสอบลงใน RSAT</span><span class="sxs-lookup"><span data-stu-id="3aff0-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="3aff0-123">เปิดไฟล์พารามิเตอร์ Excel และไปที่แท็บ **TestCaseSteps**</span><span class="sxs-lookup"><span data-stu-id="3aff0-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="3aff0-124">เมื่อต้องการตรวจสอบความถูกต้องว่าปริมาณคงคลังคงเหลือจะมากกว่า **0** ให้ไปที่ขั้นตอน **ตรวจสอบความถูกต้องของผลรวมที่พร้อมใช้งาน** และเปลี่ยนค่าจาก **411** เป็น **0**</span><span class="sxs-lookup"><span data-stu-id="3aff0-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="3aff0-125">เปลี่ยนค่าของฟิลด์ **พนักงานปฏิบัติการ** จากเครื่องหมายเท่ากับ (**=**) เป็นเครื่องหมายที่มากกว่า (**\>**)</span><span class="sxs-lookup"><span data-stu-id="3aff0-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="3aff0-126">บันทึกและปิดไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="3aff0-127">เลือก **อัปโหลด** เพื่อบันทึกการเปลี่ยนแปลงที่คุณทำไว้กับไฟล์พารามิเตอร์ Excel เป็น Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3aff0-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="3aff0-128">ขณะนี้ ถ้าค่าของฟิลด์ **ทั้งหมดพร้อมใช้งาน** สำหรับสินค้าที่ระบุในสินค้าคงคลังมีมากกว่า 0 (ศูนย์) การทดสอบจะผ่าน โดยไม่คำนึงถึงมูลค่าของปริมาณคงคลังคงเหลือจริง</span><span class="sxs-lookup"><span data-stu-id="3aff0-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="3aff0-129">ตัวแปรที่บันทึกไว้และการเชื่อมโยงของกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="3aff0-130">คุณลักษณะที่สำคัญอย่างหนึ่งของ RSAT คือการเชื่อมโยงของกรณีการทดสอบ นั่นคือ ความสามารถของการทดสอบเพื่อส่งผ่านตัวแปรไปยังการทดสอบอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="3aff0-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="3aff0-131">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความ [คัดลอกตัวแปรไปยังกรณีทดสอบลำดับ](rsat-chain-test-cases.md)</span><span class="sxs-lookup"><span data-stu-id="3aff0-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="3aff0-132">กรณีการทดสอบที่สืบทอดมา</span><span class="sxs-lookup"><span data-stu-id="3aff0-132">Derived test case</span></span>

<span data-ttu-id="3aff0-133">RSAT ช่วยให้คุณสามารถใช้งานการบันทึกงานเดียวกันกับกรณีการทดสอบหลายตัว ซึ่งช่วยให้งานรันกับการตั้งค่าคอนฟิกข้อมูลต่างๆ</span><span class="sxs-lookup"><span data-stu-id="3aff0-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="3aff0-134">ดูที่บทความ [กรณีการทดสอบที่ได้รับมา](rsat-derived-test-cases.md) สำหรับข้อมูลเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3aff0-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="3aff0-135">ตรวจสอบการแจ้งเตือนและข้อความ</span><span class="sxs-lookup"><span data-stu-id="3aff0-135">Validate notifications and messages</span></span>

<span data-ttu-id="3aff0-136">สามารถใช้คุณลักษณะนี้เพื่อตรวจสอบว่าเกิดการดำเนินการขึ้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3aff0-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="3aff0-137">ตัวอย่างเช่น เมื่อใบสั่งผลิตถูกสร้าง ประมาณการ จนถึงเริ่มต้นการผลิต แอปจะแสดงข้อความ "การผลิต – เริ่มต้น" เพื่อแจ้งให้คุณทราบว่าใบสั่งผลิตเริ่มดำเนินการแล้ว</span><span class="sxs-lookup"><span data-stu-id="3aff0-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![การผลิต – เริ่มการแจ้งเตือน](./media/use_rsa_tool_05.png)

<span data-ttu-id="3aff0-139">คุณสามารถตรวจสอบความถูกต้องของข้อความนี้ผ่าน RSAT โดยการป้อนข้อความในแท็บ **MessageValidation** ของไฟล์พารามิเตอร์ Excel สำหรับการบันทึกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3aff0-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![แท็บการตรวจสอบความถูกต้องของข้อความ](./media/use_rsa_tool_06.png)

<span data-ttu-id="3aff0-141">หลังจากรันกรณีการทดสอบ ข้อความในไฟล์พารามิเตอร์ของ Excel จะถูกเปรียบเทียบกับข้อความที่แสดง</span><span class="sxs-lookup"><span data-stu-id="3aff0-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="3aff0-142">ถ้าข้อความไม่ตรงกัน กรณีการทดสอบจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="3aff0-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="3aff0-143">คุณสามารถป้อนข้อความมากกว่าหนึ่งข้อความได้บนแท็บ **MessageValidation** ในไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="3aff0-144">นอกจากนี้ ข้อความอาจเป็นข้อผิดพลาดหรือข้อความเตือน แทนที่จะเป็นข้อความที่ให้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3aff0-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="3aff0-145">สแนปช็อต</span><span class="sxs-lookup"><span data-stu-id="3aff0-145">Snapshot</span></span>

<span data-ttu-id="3aff0-146">คุณลักษณะนี้จะจับภาพหน้าจอของขั้นตอนที่ดำเนินการในระหว่างการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="3aff0-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="3aff0-147">มีประโยชน์สำหรับการตรวจสอบหรือการดีบักจุดประสงค์</span><span class="sxs-lookup"><span data-stu-id="3aff0-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="3aff0-148">เมื่อต้องการใช้คุณลักษณะนี้ เปิดไฟล์ **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ภายใต้โฟลเดอร์การติดตั้ง RSAT (ตัวอย่างเช่น **C:\\Program Files (x86)\\Regression Suite Automation Tool**) และเปลี่ยนค่าขององค์ประกอบต่อไปนี้จาก **เท็จ** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="3aff0-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="3aff0-149">เมื่อคุณรันกรณีการทดสอบ RSAT จะสร้างสแนปช็อต (รูปภาพ) ของขั้นตอนในโฟลเดอร์การเล่นของกรณีการทดสอบในไดเรกทอรีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3aff0-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="3aff0-150">ถ้าคุณกำลังใช้เวอร์ชันที่เก่ากว่าของ RSAT รูปภาพจะถูกบันทึกไปที่ **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** โฟลเดอร์แยกต่างหากถูกสร้างขึ้นสำหรับกรณีการทดสอบแต่ละกรณีที่มีการรัน</span><span class="sxs-lookup"><span data-stu-id="3aff0-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="3aff0-151">การกำหนด</span><span class="sxs-lookup"><span data-stu-id="3aff0-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="3aff0-152">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-152">Scenario</span></span>

1. <span data-ttu-id="3aff0-153">โปรแกรมออกแบบผลิตภัณฑ์จะสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="3aff0-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="3aff0-154">ผู้จัดการฝ่ายผลิตเริ่มต้นใบสั่งผลิตเพื่อนำระดับสินค้าคงคลังไปที่สองชิ้น</span><span class="sxs-lookup"><span data-stu-id="3aff0-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="3aff0-155">การผลิตจะเริ่มต้นและสิ้นสุดใบสั่งผลิต และตรวจสอบว่าปริมาณคงคลังคงเหลือคือสองชิ้น</span><span class="sxs-lookup"><span data-stu-id="3aff0-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="3aff0-156">ทีมงานขายได้รับใบสั่งสำหรับผลิตภัณฑ์ใหม่สี่ชิ้น</span><span class="sxs-lookup"><span data-stu-id="3aff0-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="3aff0-157">ดังนั้น ทีมขายจึงปรับปรุงความต้องการสุทธิผ่านแผนแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="3aff0-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="3aff0-158">เนื่องจากไม่มีกำลังการผลิตเพิ่มเติม จะมีการตั้งค่านโยบายใบสั่งเริ่มต้นเป็น "ซื้อแทนที่จะทำ"</span><span class="sxs-lookup"><span data-stu-id="3aff0-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="3aff0-159">ดังนั้น แผนการใบสั่งซื้อจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3aff0-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="3aff0-160">ผู้ซื้อจะเพิ่มผู้จัดจำหน่าย ยืนยันแผนการใบสั่งซื้อ แล้วจากนั้น ยืนยันใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="3aff0-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="3aff0-161">เมื่อสินค้าที่ซื้อมาถึงที่ร้านค้า ผู้ปฏิบัติงานร้านค้าจะค้นหาใบสั่งซื้อที่เกี่ยวข้อง และรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="3aff0-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="3aff0-162">เนื่องจากใบสั่งนี้เสร็จสมบูรณ์แล้วในขณะนี้ คุณสามารถเบิกสินค้าและบรรจุสินค้าตามใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="3aff0-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="3aff0-163">การเงินลงรายการบัญชีใบแจ้งหนี้การซื้อและใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="3aff0-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="3aff0-164">ภาพประกอบต่อไปนี้แสดงโฟลว์สำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="3aff0-164">The following illustration shows the flow for this scenario.</span></span>

![โฟลว์สำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_14.png)

<span data-ttu-id="3aff0-166">ภาพประกอบต่อไปนี้แสดงลำดับชั้นกระบวนการทางธุรกิจสำหรับสถานการณ์จำลองนี้ใน LCS Business Process Modeler</span><span class="sxs-lookup"><span data-stu-id="3aff0-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![กระบวนการทางธุรกิจสำหรับสถานการณ์จำลองการสาธิต](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="3aff0-168">กลยุทธ์ – การเรียนรู้ที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="3aff0-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="3aff0-169">ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3aff0-169">Data</span></span>

- <span data-ttu-id="3aff0-170">ตรวจสอบให้แน่ใจว่าคุณมีปริมาณข้อมูลของตัวแทน (สำเนาของข้อมูลการตั้งค่าคอนฟิกการผลิต/แบบ golden รวมถึงข้อมูลที่ถูกย้าย)</span><span class="sxs-lookup"><span data-stu-id="3aff0-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="3aff0-171">เมื่อคุณสร้างข้อมูลใหม่ผ่านตัวบันทึกงาน ให้สร้างชื่อการทดสอบที่จะไม่ขัดแย้งกับชื่อที่มีอยู่ (ตัวอย่างเช่น ใช้คำนำหน้า เช่น **RSATxxx**)</span><span class="sxs-lookup"><span data-stu-id="3aff0-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="3aff0-172">ใช้การคืนค่า Azure Point-In-Time เพื่อรันการทดสอบในสภาพแวดล้อมที่ไม่ใช่ระดับ 1 อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3aff0-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="3aff0-173">ถึงแม้ว่าคุณจะสามารถใช้ฟังก์ชัน Excel **RANDOM** และ **NOW** เพื่อสร้างชุดที่ไม่ซ้ำกันได้ แต่ความพยายามจะสูงอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="3aff0-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="3aff0-174">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="3aff0-175">ตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="3aff0-175">Task recorder</span></span>

- <span data-ttu-id="3aff0-176">กำหนดสถานการณ์จำลอง ก่อนที่คุณจะเริ่มการบันทึก</span><span class="sxs-lookup"><span data-stu-id="3aff0-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="3aff0-177">โครงการที่มีการจัดการอย่างดีมีสถานการณ์จำลองการทดสอบที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="3aff0-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="3aff0-178">เมื่อต้องการสร้างกรณีการทดสอบ ให้พิจารณาว่าผลลัพธ์ของสถานการณ์จำลองของการทดสอบดังกล่าวสามารถคาดการณ์ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="3aff0-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="3aff0-179">แบ่งการบันทึก ถ้ามีการดำเนินการโดยบทบาทต่างๆ หรือหากมีเวลารอ หรือเหตุการณ์ภายนอกก่อนขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3aff0-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="3aff0-180">หลีกเลี่ยงการเลือกค่าในรายการ</span><span class="sxs-lookup"><span data-stu-id="3aff0-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="3aff0-181">แต่ใช้รูปแบบข้อความ เช่น **FIFO** **AudioRM** และ **SiteWH** แทน</span><span class="sxs-lookup"><span data-stu-id="3aff0-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="3aff0-182">เมื่อคุณเลือกในรายการ จะมีการบันทึกตำแหน่งของค่าในรายการ ไม่ใช่ตัวค่าเอง</span><span class="sxs-lookup"><span data-stu-id="3aff0-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="3aff0-183">ถ้ามีการเพิ่มสินค้าลงในรายการดังกล่าว ตำแหน่งของมูลค่าอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="3aff0-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="3aff0-184">ดังนั้น การบันทึกของคุณจะใช้พารามิเตอร์ที่แตกต่างกัน และส่วนที่เหลือของสถานการณ์จำลองดังกล่าวอาจได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="3aff0-185">ลองนึกถึงลักษณะการทำงานของผู้ใช้หลายราย</span><span class="sxs-lookup"><span data-stu-id="3aff0-185">Think about multi-user behavior.</span></span> <span data-ttu-id="3aff0-186">ตัวอย่างเช่น อย่าสันนิษฐานว่าใบสั่งขายที่สร้างขึ้นใหม่ของคุณจะถูกเลือกโดยอัตโนมัติเสมอ</span><span class="sxs-lookup"><span data-stu-id="3aff0-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="3aff0-187">แต่ใช้ตัวกรองเพื่อค้นหาใบสั่งที่ถูกต้องแทนเสมอ</span><span class="sxs-lookup"><span data-stu-id="3aff0-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="3aff0-188">ใช้ฟังก์ชันคัดลอกในตัวบันทึกงานเพื่อบันทึกชื่อของผลิตภัณฑ์ที่สร้างขึ้นใหม่ เพื่อให้สามารถใช้งานได้ในกรณีการทดสอบที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="3aff0-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="3aff0-189">ใช้ฟังก์ชันตรวจสอบความถูกต้องในตัวบันทึกงาน เพื่อตั้งค่าจุดตรวจสอบว่ามีการรันขั้นตอนอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3aff0-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="3aff0-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="3aff0-190">RSAT</span></span>

- <span data-ttu-id="3aff0-191">เมื่อต้องการรันการทดสอบในบริษัทอื่น คุณสามารถเปลี่ยนบริษัทบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="3aff0-192">ตรวจสอบให้แน่ใจว่าการตั้งค่าและข้อมูลพร้อมใช้งานในบริษัทที่เลือกใหม่</span><span class="sxs-lookup"><span data-stu-id="3aff0-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="3aff0-193">คุณสามารถเปลี่ยนผู้ใช้การทดสอบบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="3aff0-194">ระบุรหัสอีเมลของผู้ใช้ที่จะรันกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="3aff0-195">ในลักษณะนี้ อาจมีการรันกรณีการทดสอบโดยใช้สิทธิ์การรักษาความปลอดภัยของผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="3aff0-196">เมื่อต้องการรอก่อนที่จะเริ่มต้นการทดสอบ คุณสามารถกำหนดการหยุดชั่วคราวบนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="3aff0-197">สามารถใช้การหยุดชั่วคราวนี้ในชุดงาน (ตัวอย่างเช่น ถ้าต้องรันลำดับงานก่อนที่จะสามารถดำเนินการขั้นตอนต่อไป)</span><span class="sxs-lookup"><span data-stu-id="3aff0-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="3aff0-198">การเขียนสคริปต์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="3aff0-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="3aff0-199">CLI</span><span class="sxs-lookup"><span data-stu-id="3aff0-199">CLI</span></span>

<span data-ttu-id="3aff0-200">RSAT สามารถถูกเรียกจากหน้าต่าง **พร้อมต์คำสั่ง** หรือ **PowerShell**</span><span class="sxs-lookup"><span data-stu-id="3aff0-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="3aff0-201">ตรวจสอบว่าตัวแปรของสภาพแวดล้อม **TestRoot** ถูกตั้งค่าเป็นพาธการติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="3aff0-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="3aff0-202">(ใน Microsoft Windows เปิด **แผงควบคุม** เลือก **ระบบและการรักษาความปลอดภัย \> ระบบ \> การตั้งค่าระบบขั้นสูง** และจากนั้น เลือก **ตัวแปรของสภาพแวดล้อม** )</span><span class="sxs-lookup"><span data-stu-id="3aff0-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="3aff0-203">เปิดหน้าต่าง **พร้อมต์คำสั่ง** หรือ **PowerShell** เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="3aff0-204">นำทางไปยังไดเรกทอรีการติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="3aff0-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="3aff0-205">แสดงรายการคำสั่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3aff0-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="3aff0-206">?</span><span class="sxs-lookup"><span data-stu-id="3aff0-206">?</span></span>

<span data-ttu-id="3aff0-207">แสดงวิธีใช้เกี่ยวกับคำสั่งที่มีอยู่ทั้งหมดและพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="3aff0-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="3aff0-208">?: พารามิเตอร์ที่ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-208">?: Optional parameters</span></span>

<span data-ttu-id="3aff0-209">`command`: ที่ซึ่ง ``[command]`` เป็นหนึ่งในคำสั่งที่ระบุไว้ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="3aff0-210">เกี่ยวกับ</span><span class="sxs-lookup"><span data-stu-id="3aff0-210">about</span></span>

<span data-ttu-id="3aff0-211">แสดงรุ่นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3aff0-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="3aff0-212">cls</span><span class="sxs-lookup"><span data-stu-id="3aff0-212">cls</span></span>

<span data-ttu-id="3aff0-213">ล้างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="3aff0-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="3aff0-214">ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="3aff0-214">download</span></span>

<span data-ttu-id="3aff0-215">ดาวน์โหลดเอกสารแนบสำหรับกรณีทดสอบที่ระบุไปยังไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="3aff0-216">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="3aff0-217">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="3aff0-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="3aff0-218">ดาวน์โหลด: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-218">download: required parameters</span></span>

+ <span data-ttu-id="3aff0-219">`test_case_id`: แสดงรหัสกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="3aff0-220">`output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="3aff0-221">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="3aff0-222">ดาวน์โหลด: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="3aff0-223">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="3aff0-223">edit</span></span>

<span data-ttu-id="3aff0-224">อนุญาตให้คุณเปิดไฟล์พารามิเตอร์ในโปรแกรม Excel และแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="3aff0-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="3aff0-225">แก้ไข: พารามิเตอร์ที่ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-225">edit: required parameters</span></span>

+ <span data-ttu-id="3aff0-226">`excel_file`: ต้องมีพาธเต็มไปยังไฟล์ Excel ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="3aff0-227">แก้ไข: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="3aff0-228">สร้าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-228">generate</span></span>

<span data-ttu-id="3aff0-229">สร้างการดำเนินการทดสอบและไฟล์พารามิเตอร์สำหรับกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="3aff0-230">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="3aff0-231">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="3aff0-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="3aff0-232">สร้าง: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-232">generate: required parameters</span></span>

+ <span data-ttu-id="3aff0-233">`test_case_id`: แสดงรหัสกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="3aff0-234">`output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="3aff0-235">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="3aff0-236">สร้าง: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="3aff0-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="3aff0-237">generatederived</span></span>

<span data-ttu-id="3aff0-238">สร้างกรณีการทดสอบใหม่ซึ่งสืบทอดมาจากกรณีการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="3aff0-239">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="3aff0-240">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="3aff0-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="3aff0-241">generatederived: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="3aff0-242">`parent_test_case_id`: แสดงรหัสกรณีทดสอบหลัก</span><span class="sxs-lookup"><span data-stu-id="3aff0-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="3aff0-243">`test_plan_id`: แสดงรหัสแผนทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="3aff0-244">`test_suite_id`: แสดงรหัสชุดทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="3aff0-245">generatederived: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="3aff0-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="3aff0-246">generatetestonly</span></span>

<span data-ttu-id="3aff0-247">สร้างเฉพาะไฟล์การดำเนินการทดสอบและกรณีทดสอบที่ระบุในไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="3aff0-248">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="3aff0-249">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="3aff0-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="3aff0-250">generatetestonly: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="3aff0-251">`test_case_id`: แสดงรหัสกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="3aff0-252">`output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="3aff0-253">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="3aff0-254">generatetestonly: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="3aff0-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="3aff0-255">generatetestsuite</span></span>

<span data-ttu-id="3aff0-256">สร้างกรณีการทดสอบทั้งหมดสำหรับชุดที่ระบุในไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="3aff0-257">คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="3aff0-258">ใช้ค่าใดๆ จากคอลัมน์เป็นพารามิเตอร์ **test_suite_name**</span><span class="sxs-lookup"><span data-stu-id="3aff0-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="3aff0-259">generatetestsuite: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="3aff0-260">`test_suite_name`: แสดงชื่อชุดทดสอบ</span><span class="sxs-lookup"><span data-stu-id="3aff0-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="3aff0-261">`output_dir`: แสดงถึงไดเรกทอรีผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3aff0-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="3aff0-262">ต้องมีไดเรกทอรีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="3aff0-263">generatetestsuite: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="3aff0-264">วิธีใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-264">help</span></span>

<span data-ttu-id="3aff0-265">เหมือนกับ [?](#section)</span><span class="sxs-lookup"><span data-stu-id="3aff0-265">Identical to the [?](#section)</span></span> <span data-ttu-id="3aff0-266">คำสั่ง</span><span class="sxs-lookup"><span data-stu-id="3aff0-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="3aff0-267">รายการ</span><span class="sxs-lookup"><span data-stu-id="3aff0-267">list</span></span>

<span data-ttu-id="3aff0-268">แสดงรายการกรณีที่มีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="3aff0-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="3aff0-269">listtestplans</span></span>

<span data-ttu-id="3aff0-270">แสดงรายการแผนการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="3aff0-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="3aff0-271">listtestsuite</span></span>

<span data-ttu-id="3aff0-272">แสดงรายการกรณีทดสอบสำหรับชุดการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="3aff0-273">คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="3aff0-274">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**</span><span class="sxs-lookup"><span data-stu-id="3aff0-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="3aff0-275">listtestsuite: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="3aff0-276">`suite_name`: ชื่อของชุดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3aff0-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="3aff0-277">listtestesite: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="3aff0-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="3aff0-278">listtestsuitenames</span></span>

<span data-ttu-id="3aff0-279">แสดงรายการชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="3aff0-280">ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="3aff0-280">playback</span></span>

<span data-ttu-id="3aff0-281">ย้อนกลับกรณีการทดสอบโดยใช้ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="3aff0-282">ย้อนกลับ: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-282">playback: required parameters</span></span>

+ <span data-ttu-id="3aff0-283">`excel_file`: พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="3aff0-284">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="3aff0-285">ย้อนกลับ: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="3aff0-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="3aff0-286">playbackbyid</span></span>

<span data-ttu-id="3aff0-287">ย้อนกลับกรณีการทดสอบหลายกรณีพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="3aff0-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="3aff0-288">คุณสามารถใช้คำสั่ง ``list`` เพื่อเรียกใช้กรณีการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="3aff0-289">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **test_case_id**</span><span class="sxs-lookup"><span data-stu-id="3aff0-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="3aff0-290">playbackbyid: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="3aff0-291">`test_case_id1`: รหัสของกรณีทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="3aff0-292">`test_case_id2`: รหัสของกรณีทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="3aff0-293">`test_case_idN`: รหัสของกรณีทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="3aff0-294">playbackbyid: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="3aff0-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="3aff0-295">playbackmany</span></span>

<span data-ttu-id="3aff0-296">ย้อนกลับกรณีทดสอบหลายกรณีพร้อมกันโดยใช้ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="3aff0-297">playbackmany: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="3aff0-298">`excel_file1`: พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="3aff0-299">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-299">File must exist.</span></span>
+ <span data-ttu-id="3aff0-300">`excel_file2`: พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="3aff0-301">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-301">File must exist.</span></span>
+ <span data-ttu-id="3aff0-302">`excel_fileN`: พาธแบบเต็มไปที่ไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3aff0-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="3aff0-303">ต้องมีไฟล์อยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="3aff0-304">playbackmany: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="3aff0-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="3aff0-305">playbacksuite</span></span>

<span data-ttu-id="3aff0-306">ย้อนกลับกรณีทดสอบทั้งหมดจากชุดทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="3aff0-307">คุณสามารถใช้คำสั่ง ``listtestsuitenames`` เพื่อเรียกใช้ชุดการทดสอบทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3aff0-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="3aff0-308">ใช้ค่าใดๆ จากคอลัมน์แรกเป็นพารามิเตอร์ **suite_name**</span><span class="sxs-lookup"><span data-stu-id="3aff0-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="3aff0-309">playbacksuite: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="3aff0-310">`suite_name`: ชื่อของชุดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3aff0-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="3aff0-311">playbacksuite: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="3aff0-312">ออก</span><span class="sxs-lookup"><span data-stu-id="3aff0-312">quit</span></span>

<span data-ttu-id="3aff0-313">ปิดแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3aff0-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="3aff0-314">อัพโหลด</span><span class="sxs-lookup"><span data-stu-id="3aff0-314">upload</span></span>

<span data-ttu-id="3aff0-315">อัพโหลดไฟล์ทั้งหมดที่เป็นของชุดทดสอบหรือกรณีการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="3aff0-316">อัปโหลด: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-316">upload: required parameters</span></span>

+ <span data-ttu-id="3aff0-317">`suite_name`: ไฟล์ทั้งหมดที่เป็นของชุดทดสอบที่ระบุจะถูกอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="3aff0-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="3aff0-318">`testcase_id`: ไฟล์ทั้งหมดที่เป็นของกรณีทดสอบที่ระบุจะถูกอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="3aff0-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="3aff0-319">อัปโหลด: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="3aff0-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="3aff0-320">uploadrecording</span></span>

<span data-ttu-id="3aff0-321">อัพโหลดเฉพาะไฟล์การบันทึกที่เป็นของกรณีการทดสอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3aff0-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="3aff0-322">uploadrecording: พารามิเตอร์ที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="3aff0-323">`testcase_id`: ไฟล์การบันทึกที่เป็นของกรณีการทดสอบที่ระบุจะถูกอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="3aff0-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="3aff0-324">uploadrecording: ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3aff0-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="3aff0-325">การใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-325">usage</span></span>

<span data-ttu-id="3aff0-326">แสดงวิธีสองวิธีในการเรียกใช้แอพลิเคชันนี้: วิธีหนึ่งโดยใช้ไฟล์การตั้งค่าเริ่มต้น อีกวิธีหนึ่งให้ไฟล์การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3aff0-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="3aff0-327">ตัวอย่างของ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3aff0-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="3aff0-328">รันกรณีการทดสอบในลูป</span><span class="sxs-lookup"><span data-stu-id="3aff0-328">Run a test case in a loop</span></span>

<span data-ttu-id="3aff0-329">คุณมีสคริปต์การทดสอบที่สร้างลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="3aff0-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="3aff0-330">โดยการเขียนสคริปต์ อาจมีการรันกรณีการทดสอบนี้ในลูปโดยการสุ่มข้อมูลต่อไปนี้ ก่อนที่จะมีการรันการเกิดซ้ำแต่ละครั้ง:</span><span class="sxs-lookup"><span data-stu-id="3aff0-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="3aff0-331">รหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3aff0-331">Customer ID</span></span>
- <span data-ttu-id="3aff0-332">ชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3aff0-332">Customer name</span></span>
- <span data-ttu-id="3aff0-333">ที่อยู่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3aff0-333">Customer address</span></span>

<span data-ttu-id="3aff0-334">รหัสลูกค้าจะอยู่ในรูปแบบ *ATCUS\<number\>* โดยที่ \<number\> อยู่ระหว่าง **000000001** และ **999999999**</span><span class="sxs-lookup"><span data-stu-id="3aff0-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="3aff0-335">ตัวอย่างต่อไปนี้ใช้พารามิเตอร์ **เริ่มต้น** เพื่อกำหนดหมายเลขแรกที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="3aff0-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="3aff0-336">ใช้พารามิเตอร์ที่สอง **nr** เพื่อกำหนดจำนวนของลูกค้าที่ต้องสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3aff0-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="3aff0-337">สำหรับการเกิดซ้ำแต่ละครั้ง จะมีการเปลี่ยนแปลงพารามิเตอร์ในไฟล์พารามิเตอร์ Excel โดยใช้ฟังก์ชัน UpdateCustomer</span><span class="sxs-lookup"><span data-stu-id="3aff0-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="3aff0-338">จากนั้น รายการคำสั่ง RSAT ถูกเรียกในฟังก์ชัน RunTestCase</span><span class="sxs-lookup"><span data-stu-id="3aff0-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="3aff0-339">เปิด Microsoft Windows PowerShell Integrated Scripting Environment (ISE) ในโหมดผู้ดูแลระบบ และวางรหัสต่อไปนี้ลงในหน้าต่างที่ชื่อ **Untitled1.ps1**</span><span class="sxs-lookup"><span data-stu-id="3aff0-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="3aff0-340">รันสคริปต์ที่ขึ้นอยู่กับข้อมูลใน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3aff0-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="3aff0-341">ตัวอย่างต่อไปนี้ใช้การเรียก Open Data Protocol (OData) ในการค้นหาสถานะใบสั่งของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="3aff0-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="3aff0-342">ถ้าสถานะยังไม่ได้ **ออกใบแจ้งหนี้** คุณสามารถ ตัวอย่างเช่น เรียกใช้กรณีการทดสอบ RSAT ที่ลงรายการบัญชีใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="3aff0-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]