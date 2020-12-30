---
title: ทำให้การทดสอบเป็นแบบอัตโนมัติด้วยการรายงานทางอิเล็กทรอนิกส์
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถใช้คุณลักษณะพื้นฐานของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำให้การทดสอบของฟังก์ชันเป็นแบบอัตโนมัติ
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0a2586afd56eef0f953454ad246ff3647a5b09d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681459"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="89745-103">ดำเนินการทดสอบอัตโนมัติกับการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="89745-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="89745-104">หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถใช้กรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำให้การทดสอบของบางฟังก์ชันเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="89745-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="89745-105">ตัวอย่างในหัวข้อนี้จะแสดงวิธีการทำให้การทดสอบของการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="89745-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="89745-106">แอพลิเคชันใช้กรอบงาน ER เพื่อสร้างไฟล์การชำระเงินและเอกสารที่เกี่ยวข้องในระหว่างการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="89745-107">กรอบงาน ER ประกอบด้วย แบบจำลองข้อมูล การแม็ปแบบจำลอง และส่วนประกอบรูปแบบที่สนับสนุนการประมวลผลการชำระเงินสำหรับชนิดการชำระเงินที่แตกต่างกัน และการสร้างเอกสารในรูปแบบที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="89745-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="89745-108">สามารถดาวน์โหลดส่วนประกอบเหล่านี้ได้จาก Microsoft Dynamics Lifecycle Services (LCS) และสามารถนำเข้าไปยังอินสแตนซ์ได้</span><span class="sxs-lookup"><span data-stu-id="89745-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="89745-109">นอกจากนี้ คุณยังสามารถปรับแต่งแต่ละองค์ประกอบของ Microsoft และใช้เป็นพื้นฐานของส่วนประกอบที่กำหนดเองของคุณได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="89745-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="89745-110">โดยการสร้างรุ่นที่กำหนดเอง คุณสามารถทำการเปลี่ยนแปลงที่สนับสนุนความต้องการที่เฉพาะเจาะจงได้</span><span class="sxs-lookup"><span data-stu-id="89745-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="89745-111">ตัวอย่างเช่น คุณสามารถปรับปรุงแบบจำลองข้อมูล ER และการแม็ปแบบจำลอง ER เพื่อเข้าถึงข้อมูลแอพลิเคชันเฉพาะลูกค้า หรือคุณสามารถเปลี่ยนรูปแบบ ER เพื่อแก้ไขโครงร่างของเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="89745-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="89745-112">คุณสามารถใช้รูปแบบ ER แบบกำหนดเองในอินสแตนซ์ เพื่อประมวลผลไฟล์การชำระเงินที่สร้างการชำระเงินให้แก่ผู้จัดจำหน่าย และเพื่อประมวลผลรายงานการควบคุมด้วย</span><span class="sxs-lookup"><span data-stu-id="89745-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="89745-113">การกำหนดรุ่นได้รับการสนับสนุนในส่วนประกอบ ER</span><span class="sxs-lookup"><span data-stu-id="89745-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="89745-114">ดังนั้น Microsoft จึงสามารถให้โซลูชัน ER รุ่นที่ปรับปรุงสำหรับการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย และคุณสามารถผสานรุ่นที่ปรับปรุงโดยอัตโนมัติกับส่วนประกอบที่กำหนดเองของคุณได้โดยการปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="89745-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="89745-115">อย่างไรก็ตาม คุณต้องทดสอบรุ่นที่ปรับใช้ซ้ำเพื่อตรวจสอบให้แน่ใจว่าจะทำงานได้ตามที่คุณคาดไว้</span><span class="sxs-lookup"><span data-stu-id="89745-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="89745-116">แบบจำลองข้อมูล ER และการแม็ปการแบบจำลอง ER ใช้ร่วมกันสำหรับรูปแบบ ER หลายแบบที่ใช้ในการประมวลผลการชำระเงินชนิดต่างๆ และเพื่อสร้างเอกสารการชำระเงินเฉพาะประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="89745-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="89745-117">ดังนั้น จึงน่าพึงพอใจอย่างมากที่จะทำให้การทดสอบการยอมรับและการรวมของผู้ใช้เป็นแบบอัตโนมัติ เพื่อให้สามารถดำเนินการได้โดยอัตโนมัติในบริษัทหลากหลายแห่ง แต่คำนึงถึงบริบทประเทศ/ภูมิภาคของบริษัทปลายทางแต่ละแห่ง ใช้ชุดข้อมูลที่แตกต่างกัน และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="89745-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="89745-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างรุ่นที่กำหนดเองของรูปแบบที่ขึ้นอยู่กับรูปแบบที่คุณได้รับจากผู้ให้บริการการตั้งค่าคอนฟิก ดู [ER ปรับรุ่นรูปแบบของคุณโดยปรับใช้รุ่นพื้นฐานใหม่ของรูปแบบนั้น](./tasks/er-upgrade-format.md)</span><span class="sxs-lookup"><span data-stu-id="89745-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="89745-119">แนวคิดหลัก</span><span class="sxs-lookup"><span data-stu-id="89745-119">Key concepts</span></span>

<span data-ttu-id="89745-120">ผู้ใช้ระดับสูงด้านการใช้งานสามารถสร้างการทดสอบการยอมรับและการรวมของผู้ใช้ได้ โดยไม่ต้องเขียนรหัสต้นทาง</span><span class="sxs-lookup"><span data-stu-id="89745-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="89745-121">ใช้คุณลักษณะพื้นฐาน ER เพื่อเปรียบเทียบเอกสารที่สร้างขึ้นกับสำเนาหลัก</span><span class="sxs-lookup"><span data-stu-id="89745-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="89745-122">สำหรับข้อมูลเพิ่มเติม ดู [ติดตามผลรายงานที่สร้างขึ้น และเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md)</span><span class="sxs-lookup"><span data-stu-id="89745-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="89745-123">ใช้ตัวบันทึกงานเพื่อบันทึกกรณีทดสอบ และรวมการประเมินพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="89745-124">สำหรับข้อมูลเพิ่มเติม ดูที่ [ทรัพยากรตัวบันทึกงาน](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="89745-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="89745-125">กรณีการทดสอบกลุ่มสำหรับสถานการณ์จำลองการทดสอบที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="89745-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="89745-126">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างและดำเนินการทดสอบการยอมรับของผู้ใช้อัตโนมัติ](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)</span><span class="sxs-lookup"><span data-stu-id="89745-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="89745-127">ใช้ตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM) ใน LCS เพื่อสร้างไลบรารีสำหรับการทดสอบการยอมรับของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="89745-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="89745-128">ใช้ไลบรารีสำหรับการทดสอบ BPM เพื่อสร้างแผนการทดสอบ และทดสอบชุดใน Microsoft Azure DevOps Services (Azure DevOps)</span><span class="sxs-lookup"><span data-stu-id="89745-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="89745-129">ผู้ใช้ระดับสูงด้านการใช้งานสามารถรันการทดสอบการยอมรับและการรวมของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="89745-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="89745-130">ใช้ Regression Suite Automation Tool (RSAT) เพื่อรันกรณีทดสอบของชุดทดสอบที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="89745-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="89745-131">รายงานผลลัพธ์ของการทดสอบไปยัง Azure DevOps และใช้บริการนี้เพื่อตรวจสอบผลลัพธ์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="89745-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="89745-132">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="89745-132">Prerequisites</span></span>

<span data-ttu-id="89745-133">ก่อนที่คุณจะสามารถทำงานให้เสร็จสมบูรณ์ในหัวข้อนี้ คุณต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="89745-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="89745-134">ปรับใช้โทโพโลยีที่สนับสนุนการทดสอบแบบระบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="89745-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="89745-135">คุณต้องมีสิทธิ์เข้าถึงอินสแตนซ์ของโทโพโลยีนี้สำหรับบทบาท **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="89745-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="89745-136">โทโพโลยีนี้ต้องมีข้อมูลสาธิตซึ่งจะใช้ในตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="89745-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="89745-137">สำหรับข้อมูลเพิ่มเติม ดูที่ [ปรับใช้และใช้สภาพแวดล้อมที่สนับสนุนการสร้างอย่างต่อเนื่องและระบบอัตโนมัติของการทดสอบ](../perf-test/continuous-build-test-automation.md)</span><span class="sxs-lookup"><span data-stu-id="89745-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="89745-138">เมื่อต้องการรันการทดสอบการยอมรับและการรวมของผู้ใช้โดยอัตโนมัติ คุณต้องติดตั้ง RSAT ในโทโพโลยีที่คุณกำลังใช้และตั้งค่าคอนฟิกในลักษณะที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="89745-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="89745-139">สำหรับข้อมูลเกี่ยวกับวิธีการติดตั้งและตั้งค่า RSAT และตั้งค่าคอนฟิกให้ทำงานกับแอป Finance and Operations และ Azure DevOps ดูที่ [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)</span><span class="sxs-lookup"><span data-stu-id="89745-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="89745-140">ให้ความสำคัญกับข้อกำหนดเบื้องต้นสำหรับการใช้เครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="89745-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="89745-141">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่า RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="89745-142">สี่เหลี่ยมสีน้ำเงินล้อมรอบพารามิเตอร์ที่ระบุสิทธิ์การเข้าถึง Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="89745-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="89745-143">สี่เหลี่ยมสีเขียวล้อมรอบพารามิเตอร์ที่ระบุการเข้าถึงอินสแตนซ์</span><span class="sxs-lookup"><span data-stu-id="89745-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="89745-144">![การตั้งค่า RSAT](media/GER-Configure.png "ภาพหน้าจอของกล่องโต้ตอบการตั้งค่า RSAT")</span><span class="sxs-lookup"><span data-stu-id="89745-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="89745-145">เมื่อต้องการจัดระเบียบกรณีทดสอบในชุดเพื่อช่วยรับประกันลำดับการดำเนินการที่ถูกต้อง เพื่อให้คุณสามารถรวบรวมล็อกของการดำเนินการทดสอบสำหรับการรายงานและการตรวจสอบเพิ่มเติม คุณต้องมีสิทธิเข้าถึง Azure DevOps จากโทโพโลยีที่ปรับใช้</span><span class="sxs-lookup"><span data-stu-id="89745-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="89745-146">เมื่อต้องการดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ เราขอแนะนำให้คุณดาวน์โหลด [การใช้ ER สำหรับการทดสอบ RSAT](https://go.microsoft.com/fwlink/?linkid=874684)</span><span class="sxs-lookup"><span data-stu-id="89745-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="89745-147">ไฟล์ zip นี้มีคำแนะนำเกี่ยวกับงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="89745-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="89745-148">ปริมาณความจุ</span><span class="sxs-lookup"><span data-stu-id="89745-148">Content</span></span>                                           | <span data-ttu-id="89745-149">ชื่อไฟล์และสถานที่</span><span class="sxs-lookup"><span data-stu-id="89745-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="89745-150">การบันทึกงานตัวอย่างเพื่อจัดเตรียมข้อมูลสำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="89745-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="89745-151">จัดเตรียม\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="89745-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="89745-152">การบันทึกงานตัวอย่างเพื่อประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="89745-153">ประมวลผล\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="89745-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="89745-154">จัดเตรียมโมดูลบัญชีเจ้าหนี้เพื่อประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="89745-155">ลงชื่อเข้าใช้อินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="89745-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="89745-156">ดาวน์โหลดการตั้งค่าคอนฟิก ER ต่อไปนี้จาก LCS</span><span class="sxs-lookup"><span data-stu-id="89745-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="89745-157">สำหรับคำแนะนำ ดู [ER นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md)</span><span class="sxs-lookup"><span data-stu-id="89745-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="89745-158">การตั้งค่าคอนฟิกแบบจำลอง ER ของ **แบบจำลองการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="89745-159">การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ของ **การแม็ปแบบจำลองการชำระเงิน 1611**</span><span class="sxs-lookup"><span data-stu-id="89745-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="89745-160">**BACS (UK)** การตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="89745-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="89745-161">![การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์](media/GER-Configurations.png "ภาพหน้าจอของหน้าการตั้งค่าคอนฟิกในการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="89745-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="89745-162">เลือกบริษัทข้อมูลสาธิต **GBSI** ซึ่งมีบริบทประเทศ/ภูมิภาคในสหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="89745-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="89745-163">ตั้งค่าคอนฟิกพารามิเตอร์บัญชีเจ้าหนี้:</span><span class="sxs-lookup"><span data-stu-id="89745-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="89745-164">ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่าการชำระเงิน \> วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="89745-165">เลือกวิธีการชำระเงิน **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="89745-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="89745-166">ตั้งค่าคอนฟิกวิธีการชำระเงินที่เลือกเพื่อให้ใช้รูปแบบ ER ของ **BACS (UK)** ที่คุณดาวน์โหลดก่อนหน้านี้ สำหรับการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="89745-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="89745-167">บน FastTab **รูปแบบไฟล์** ให้ตั้งค่าตัวเลือก **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="89745-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="89745-168">ในฟิลด์ **ส่งออกการตั้งค่าคอนฟิกรูปแบบ** ให้เลือก **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="89745-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="89745-169">![หน้าวิธีการชำระเงิน](media/GER-APParameters.png "ภาพหน้าจอของหน้าวิธีการชำระเงิน")</span><span class="sxs-lookup"><span data-stu-id="89745-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="89745-170">ถ้าคุณมีรุ่นที่ได้รับของรูปแบบ ER นี้ที่ถูกสร้างขึ้นเพื่อสนับสนุนการเลือกกำหนด คุณสามารถเลือกการตั้งค่าคอนฟิกนี้ได้ในวิธีการชำระเงิน **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="89745-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="89745-171">สร้างตัวอย่างการชำระเงินให้แก่ผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="89745-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="89745-172">ไปที่ **บัญชีเจ้าหนี้ \> การชำระเงิน \> สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="89745-173">ตรวจสอบให้แน่ใจว่าคุณยังไม่ได้ลงรายการบัญชีสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="89745-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="89745-174">![หน้าสมุดรายวันการชำระเงิน](media/GER-APJournal.png "ภาพหน้าจอของหน้าสมุดรายวันการชำระเงิน")</span><span class="sxs-lookup"><span data-stu-id="89745-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="89745-175">เลือก **รายการ** และป้อนรายการที่มีข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="89745-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="89745-176">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="89745-176">Field</span></span>               | <span data-ttu-id="89745-177">มูลค่าตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="89745-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="89745-178">ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-178">Vendor name</span></span>         | <span data-ttu-id="89745-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="89745-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="89745-180">เดบิต</span><span class="sxs-lookup"><span data-stu-id="89745-180">Debit</span></span>               | <span data-ttu-id="89745-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="89745-181">1,000.00</span></span>        |
        | <span data-ttu-id="89745-182">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="89745-182">Currency</span></span>            | <span data-ttu-id="89745-183">GBP</span><span class="sxs-lookup"><span data-stu-id="89745-183">GBP</span></span>             |
        | <span data-ttu-id="89745-184">ชนิดของบัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="89745-184">Offset account type</span></span> | <span data-ttu-id="89745-185">ธนาคาร</span><span class="sxs-lookup"><span data-stu-id="89745-185">Bank</span></span>            |
        | <span data-ttu-id="89745-186">บัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="89745-186">Offset account</span></span>      | <span data-ttu-id="89745-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="89745-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="89745-188">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="89745-188">Method of payment</span></span>   | <span data-ttu-id="89745-189">อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="89745-189">Electronic</span></span>      |

    <span data-ttu-id="89745-190">![หน้าการชำระเงินให้แก่ผู้จัดจำหน่าย](media/GER-APJournalLines.png "ภาพหน้าจอของหน้าการชำระเงินให้แก่ผู้จัดจำหน่าย")</span><span class="sxs-lookup"><span data-stu-id="89745-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="89745-191">จัดเตรียมกรอบงาน ER เพื่อทดสอบการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="89745-192">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="89745-192">Configure ER parameters</span></span>

1. <span data-ttu-id="89745-193">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="89745-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="89745-194">บนแท็บ **เอกสารแนบ** ในฟิลด์ **พื้นฐาน** เลือก **ไฟล์** เป็นชนิดเอกสารที่กรอบงานการจัดการเอกสาร (DM) ใช้เพื่อเก็บเอกสารที่เกี่ยวข้องกับคุณลักษณะพื้นฐานเป็นเอกสารแนบ DM</span><span class="sxs-lookup"><span data-stu-id="89745-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="89745-195">![หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์](media/GER-ERParameters.png "ภาพหน้าจอของหน้าพารามิเตอร์ของการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="89745-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="89745-196">สร้างสำเนาพื้นฐานของเอกสารที่เกี่ยวข้องกับการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="89745-197">ไปที่ **บัญชีเจ้าหนี้ \> การชำระเงิน \> สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="89745-198">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="89745-198">Select **Lines**.</span></span>
3. <span data-ttu-id="89745-199">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="89745-200">เลือกวิธีการชำระเงิน **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="89745-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="89745-201">เลือกบัญชีธนาคาร **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="89745-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="89745-202">ตั้งค่าตัวเลือก **พิมพ์รายงานควบคุม** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="89745-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="89745-203">ดาวน์โหลดเอาท์พุทที่สร้างเป็นไฟล์ zip</span><span class="sxs-lookup"><span data-stu-id="89745-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="89745-204">เปิดไฟล์ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="89745-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="89745-205">แยกไฟล์ต่อไปนี้จากไฟล์ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="89745-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="89745-206">ไฟล์การชำระเงินของ **ไฟล์** ในรูปแบบข้อความ</span><span class="sxs-lookup"><span data-stu-id="89745-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="89745-207">ไฟล์รายงานการควบคุม **ERVendOutPaymControlReport** ในรูปแบบ XLSX</span><span class="sxs-lookup"><span data-stu-id="89745-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="89745-208">![ไฟล์ที่แยก](media/GER-APJournalProcessed.png "ภาพหน้าจอของชื่อไฟล์ที่แยกไว้ใน Windows explorer")</span><span class="sxs-lookup"><span data-stu-id="89745-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="89745-209">เปิดใช้งานคุณลักษณะพื้นฐาน ER</span><span class="sxs-lookup"><span data-stu-id="89745-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="89745-210">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="89745-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="89745-211">บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="89745-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="89745-212">ตั้งค่าตัวเลือก **รันในโหมดดีบัก** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="89745-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="89745-213">โดยการเปิดพารามิเตอร์ **รันในโหมดดีบัก** คุณบังคับให้กรอบงาน ER ทำการดำเนินการต่อไปนี้ หลังจากการดำเนินการของรูปแบบ ER ใดๆ ที่สร้างเอกสารขาออก:</span><span class="sxs-lookup"><span data-stu-id="89745-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="89745-214">กำหนดว่ามีการตั้งค่าคอนฟิกข้อมูลพื้นฐานสำหรับส่วนประกอบใดๆ ของรูปแบบ ER ที่ดำเนินการหรือไม่</span><span class="sxs-lookup"><span data-stu-id="89745-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="89745-215">กำหนดว่าข้อมูลพื้นฐานที่ตั้งค่าคอนฟิกแต่ละรายการสามารถใช้ได้ในเงื่อนไขปัจจุบัน (รหัสบริษัทของบริษัทที่ลงชื่อเข้าใช้ ชื่อไฟล์ และนามสกุลของชื่อไฟล์ของเอาท์พุทที่สร้างขึ้น และอื่นๆ)</span><span class="sxs-lookup"><span data-stu-id="89745-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="89745-216">สำหรับข้อมูลพื้นฐานที่ใช้ได้แต่ละรายการ ให้ดำเนินการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="89745-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="89745-217">เปรียบเทียบเอาท์พุทที่สร้างขึ้นในระหว่างการดำเนินการของรูปแบบ ER กับข้อมูลพื้นฐานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="89745-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="89745-218">จัดเก็บผลลัพธ์ของการเปรียบเทียบในล็อกดีบักการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="89745-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="89745-219">ตั้งค่าคอนฟิกข้อมูลพื้นฐาน ER สำหรับการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="89745-220">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="89745-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="89745-221">เลือก **พื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="89745-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="89745-222">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89745-222">Select **New**.</span></span>
4. <span data-ttu-id="89745-223">ใน **การอ้างอิง** ให้เลือกรูปแบบ **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="89745-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="89745-224">เลือก **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="89745-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="89745-225">เพิ่มข้อมูลพื้นฐานใหม่สำหรับไฟล์การชำระเงินของผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="89745-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="89745-226">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89745-226">Select **New**.</span></span>
    2. <span data-ttu-id="89745-227">ในฟิลด์ **ชนิด** เลือกชนิดเอกสาร DM ของ **ไฟล์** ที่คุณตั้งค่าคอนฟิกไว้ในพารามิเตอร์ ER เพื่อจัดเก็บสิ่งประดิษฐ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="89745-228">เรียกดูเพื่อเลือกไฟล์การชำระเงินของ **ไฟล์** ที่บันทึกไว้เฉพาะที่ในรูปแบบข้อความ</span><span class="sxs-lookup"><span data-stu-id="89745-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="89745-229">ในฟิลด์ **คำอธิบาย** ป้อน **ไฟล์ TXT ของการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="89745-230">เพิ่มข้อมูลพื้นฐานใหม่สำหรับรายงานการควบคุมสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="89745-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="89745-231">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="89745-231">Select **New**.</span></span>
    2. <span data-ttu-id="89745-232">ในฟิลด์ **ชนิด** เลือกชนิดเอกสาร DM ของ **ไฟล์** ที่คุณตั้งค่าคอนฟิกไว้ในพารามิเตอร์ ER เพื่อจัดเก็บสิ่งประดิษฐ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="89745-233">เรียกดูเพื่อเลือกไฟล์รายงานการควบคุม **ERVendOutPaymControlReport** ที่บันทึกไว้เฉพาะที่ ในรูปแบบ XLSX</span><span class="sxs-lookup"><span data-stu-id="89745-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="89745-234">ในฟิลด์ **คำอธิบาย** ป้อน **รายงานการควบคุม XLSX ของการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="89745-235">![ข้อมูลพื้นฐานสำหรับไฟล์และรายงานการควบคุมสำหรับการชำระเงินให้แก่ผู้จัดจำหน่าย](media/GER-BaselineAttachments.png "ภาพหน้าจอของหน้าการตั้งค่าคอนฟิกที่มีรายงานการควบคุมการชำระเงิน XLSX ที่เลือก")</span><span class="sxs-lookup"><span data-stu-id="89745-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="89745-236">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89745-236">Close the page.</span></span>
9. <span data-ttu-id="89745-237">บน FastTab **พื้นฐาน** ให้เลือก **สร้าง** เพื่อตั้งค่าคอนฟิกพื้นฐานสำหรับไฟล์การชำระเงิน:</span><span class="sxs-lookup"><span data-stu-id="89745-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="89745-238">ตั้งชื่อรายการ **การตั้งค่าพื้นฐานสำหรับไฟล์การชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="89745-239">ในฟิลด์ **ชื่อส่วนประกอบไฟล์** ให้เลือก **ไฟล์** ที่จะใช้ข้อมูลพื้นฐานนี้กับเอาท์พุทของรูปแบบ ER ที่สร้างไฟล์การชำระเงินในรูปแบบข้อความ BACS (UK)</span><span class="sxs-lookup"><span data-stu-id="89745-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="89745-240">ในฟิลด์ **บริษัท** ให้เลือก **GBSI** เพื่อใช้ข้อมูลพื้นฐานนี้ เมื่อมีการรันรูปแบบ ER ของ **BACS (UK)** ในบริษัท GBSI</span><span class="sxs-lookup"><span data-stu-id="89745-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="89745-241">ในฟิลด์ **ตัวพรางชื่อไฟล์** ป้อน **\*.TXT** เพื่อใช้ข้อมูลพื้นฐานนี้เฉพาะกับเอาท์พุทของชื่อไฟล์ขององค์ประกอบรูปแบบชื่อไฟล์ **ไฟล์** ที่มีส่วนขยายนามสกุลของ **. txt**</span><span class="sxs-lookup"><span data-stu-id="89745-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="89745-242">ในฟิลด์ **ข้อมูลพื้นฐาน** เลือก **ไฟล์ของ TXT การชำระเงิน** เพื่อให้พื้นฐานนี้ใช้สำหรับการเปรียบเทียบกับผลผลิตที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="89745-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="89745-243">เลือก **สร้าง** เพื่อตั้งค่าคอนฟิกพื้นฐานสำหรับรายงานการควบคุม:</span><span class="sxs-lookup"><span data-stu-id="89745-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="89745-244">ตั้งชื่อรายการ **การตั้งค่าพื้นฐานสำหรับรายงานการควบคุม**</span><span class="sxs-lookup"><span data-stu-id="89745-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="89745-245">ในฟิลด์ **ชื่อส่วนประกอบไฟล์** ให้เลือก **ERVendOutPaymControlReport** ที่จะใช้ข้อมูลพื้นฐานนี้กับเอาท์พุทของรูปแบบ ER ที่สร้างไฟล์รายงานการควบคุม</span><span class="sxs-lookup"><span data-stu-id="89745-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="89745-246">ในฟิลด์ **บริษัท** ให้เลือก **GBSI** เพื่อใช้ข้อมูลพื้นฐานนี้ เมื่อมีการรันรูปแบบ ER ของ **BACS (UK)** ในบริษัท GBSI</span><span class="sxs-lookup"><span data-stu-id="89745-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="89745-247">ในฟิลด์ **ตัวพรางชื่อไฟล์** ป้อน **\*.XLSX** เพื่อใช้ข้อมูลพื้นฐานนี้เฉพาะกับเอาท์พุทขององค์ประกอบรูปแบบ **ERVendOutPaymControlReport** ที่มีส่วนขยายนามสกุลของ **.xslx**</span><span class="sxs-lookup"><span data-stu-id="89745-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="89745-248">ในฟิลด์ **ข้อมูลพื้นฐาน** เลือก **รายงานการควบคุมใน XLSX ของการชำระเงิน** เพื่อให้พื้นฐานนี้ถูกนี้ใช้สำหรับการเปรียบเทียบกับผลผลิตที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="89745-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="89745-249">![ข้อมูลพื้นฐานแท็บด่วนบนหน้าการตั้งค่าคอนฟิก](media/GER-BaselineRules.png "ภาพหน้าจอของแท็บด่วนข้อมูลพื้นฐานบนหน้าการตั้งค่าคอนฟิก")</span><span class="sxs-lookup"><span data-stu-id="89745-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="89745-250">บันทึกการทดสอบเพื่อตรวจสอบการประมวลผลการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="89745-251">ในฐานะผู้ใช้ระดับสูงด้านการใช้งาน คุณสามารถบันทึกขั้นตอนของคุณเองเพื่อทดสอบการประมวลผลการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="89745-252">เราขอแนะนำให้คุณเล่น (และแก้ไข ตามต้องการ) การบันทึกงาน **เตรียมการ\\Recording.xml** ที่คุณดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="89745-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="89745-253">การบันทึกนี้ใช้ในการตั้งค่าข้อมูลการทดสอบทั้งหมดไปยังสถานะที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="89745-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="89745-254">ต้องใช้ขั้นตอนนั้นเนื่องจากการทดสอบสามารถทำได้หลายครั้ง และการทดสอบทุกครั้งต้องใช้ข้อมูลที่อยู่ในสถานะเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="89745-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="89745-255">รีเซ็ตการตั้งค่าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="89745-255">Reset user settings</span></span>

1. <span data-ttu-id="89745-256">เปิดแดชบอร์ดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="89745-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="89745-257">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์รูปเฟือง)</span><span class="sxs-lookup"><span data-stu-id="89745-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="89745-258">เลือก **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="89745-258">Select **User options**.</span></span>
4. <span data-ttu-id="89745-259">เลือก **ข้อมูลการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="89745-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="89745-260">เลือก **รีเซ็ต**</span><span class="sxs-lookup"><span data-stu-id="89745-260">Select **Reset**.</span></span>
6. <span data-ttu-id="89745-261">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการรีเซ็ตข้อมูลการใช้</span><span class="sxs-lookup"><span data-stu-id="89745-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="89745-262">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="89745-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="89745-263">บันทึกขั้นตอนเพื่อจัดเตรียมข้อมูลสำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="89745-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="89745-264">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์รูปเฟือง)</span><span class="sxs-lookup"><span data-stu-id="89745-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="89745-265">เลือก **ตัวบันทึกงาน**</span><span class="sxs-lookup"><span data-stu-id="89745-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="89745-266">เลือก **เล่นการบันทึก**</span><span class="sxs-lookup"><span data-stu-id="89745-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="89745-267">เลือก **เปิดจากพีซีนี้**</span><span class="sxs-lookup"><span data-stu-id="89745-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="89745-268">เลือก **เรียกดู** และเลือกบันทึกไฟล์ **จัดเตรียม\\Recording.xml** ที่ไว้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="89745-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="89745-269">เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="89745-269">Select **Start**.</span></span>
7. <span data-ttu-id="89745-270">เลือก **เล่นขั้นตอนถัดไปที่ค้างอยู่** จนกว่าจะมีการเล่นขั้นตอนทั้งหมดในการจัดทำเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="89745-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="89745-271">การบันทึกงานนี้ทำการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="89745-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="89745-272">ตั้งค่าสถานะของรายการการชำระเงินที่ประมวลผลเป็น **None**</span><span class="sxs-lookup"><span data-stu-id="89745-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="89745-273">![ขั้นตอนการบันทึกงานที่ 3 ถึง 4](media/GER-Recording1Review1.png "ภาพหน้าจอของขั้นตอนการบันทึกงานที่ 3 ถึง 4")</span><span class="sxs-lookup"><span data-stu-id="89745-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="89745-274">เปิดใช้งานพารามิเตอร์ผู้ใช้ ER **รันในโหมดดีบัก**</span><span class="sxs-lookup"><span data-stu-id="89745-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="89745-275">![ขั้นตอนการบันทึกงานที่ 9 ถึง 10](media/GER-Recording1Review2.png "ภาพหน้าจอของขั้นตอนการบันทึกงานที่ 9 ถึง 10")</span><span class="sxs-lookup"><span data-stu-id="89745-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="89745-276">ล้างล็อกของดีบัก ER ที่ประกอบด้วย ผลลัพธ์ของการเปรียบเทียบไฟล์เอาท์พุทกับข้อมูลพื้นฐานที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="89745-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="89745-277">![ขั้นตอนการบันทึกงานที่ 13 ถึง 15](media/GER-Recording1Review3.png "ภาพหน้าจอของขั้นตอนการบันทึกงานที่ 13 ถึง 15")</span><span class="sxs-lookup"><span data-stu-id="89745-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="89745-278">บันทึกขั้นตอนเพื่อทดสอบการประมวลผลการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="89745-279">เราขอแนะนำให้คุณเล่น (และแก้ไข ตามต้องการ) การบันทึกงาน **ประมวลผล\\Recording.xml** ที่คุณดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="89745-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="89745-280">การบันทึกนี้ใช้ในการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย และตรวจสอบความถูกต้องของผลลัพธ์ของการเปรียบเทียบเอกสารที่สร้างขึ้นกับข้อมูลพื้นฐานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="89745-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="89745-281">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์รูปเฟือง)</span><span class="sxs-lookup"><span data-stu-id="89745-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="89745-282">เลือก **ตัวบันทึกงาน**</span><span class="sxs-lookup"><span data-stu-id="89745-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="89745-283">เลือก **เล่นการบันทึก**</span><span class="sxs-lookup"><span data-stu-id="89745-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="89745-284">เลือก **เปิดจากพีซีนี้**</span><span class="sxs-lookup"><span data-stu-id="89745-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="89745-285">เลือก **เรียกดู** และเลือกไฟล์ **ประมวลผล\\Recording.xml** ที่บันทึกไว้ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="89745-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="89745-286">เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="89745-286">Select **Start**.</span></span>
7. <span data-ttu-id="89745-287">เลือก **เล่นขั้นตอนถัดไปที่ค้างอยู่** จนกว่าจะมีการเล่นขั้นตอนทั้งหมดในการจัดทำเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="89745-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="89745-288">การบันทึกงานนี้ทำการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="89745-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="89745-289">เริ่มต้นการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="89745-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="89745-290">เลือกพารามิเตอร์รันไทม์ที่ถูกต้อง และเปิดการสร้างของรายงานการควบคุม</span><span class="sxs-lookup"><span data-stu-id="89745-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="89745-291">![ขั้นตอนการบันทึกงานที่ 3 ถึง 8](media/GER-Recording2Review1.png "ภาพหน้าจอของขั้นตอนการบันทึกงานที่ 3 ถึง 8")</span><span class="sxs-lookup"><span data-stu-id="89745-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="89745-292">เข้าถึงล็อกของดีบัก ER เพื่อบันทึกผลลัพธ์ของการเปรียบเทียบเอาท์พุทกับข้อมูลพื้นฐานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="89745-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="89745-293">ในล็อกดีบัก ER ผลลัพธ์ของการเปรียบเทียบจะปรากฏในฟิลด์ **ข้อความที่สร้างขึ้น**</span><span class="sxs-lookup"><span data-stu-id="89745-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="89745-294">ฟิลด์ **องค์ประกอบของรูปแบบ** และ **พาธรูปแบบที่ทำให้เกิดรายการล็อก** อ้างอิงถึงส่วนประกอบของไฟล์ที่มีการเปรียบเทียบเอาท์พุทกับข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="89745-295">![รายการในหน้าบันทึกการรันการรายงานทางอิเล็กทรอนิกส์](media/GER-ERDebugLog.png "ภาพหน้าจอของรายการในหน้าบันทึกการรันการรายงานทางอิเล็กทรอนิกส์")</span><span class="sxs-lookup"><span data-stu-id="89745-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="89745-296">การเปรียบเทียบเอาท์พุทปัจจุบันกับข้อมูลพื้นฐานจะถูกบันทึกโดยการใช้ตัวเลือกตัวบันทึกงานของ **ตรวจสอบความถูกต้อง** และการเลือก  **มูลค่าปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="89745-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="89745-297">![การใช้ตัวเลือกตรวจสอบความถูกต้องสำหรับการเปรียบเทียบกับมูลค่าปัจจุบัน](media/GER-TRRecordValidation.png "ภาพหน้าจอของการใช้ตัวเลือกตรวจสอบความถูกต้องสำหรับการเปรียบเทียบกับมูลค่าปัจจุบัน")</span><span class="sxs-lookup"><span data-stu-id="89745-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="89745-298">ภาพประกอบต่อไปนี้แสดงให้เห็นว่าขั้นตอนการตรวจสอบความถูกต้องที่บันทึกไว้มีลักษณะอย่างไรในการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="89745-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="89745-299">![ขั้นตอนการบันทึกงานที่ 13 และ 15](media/GER-Recording2Review2.png "ภาพหน้าจอของขั้นตอนการบันทึกงานที่ 13 และ 15")</span><span class="sxs-lookup"><span data-stu-id="89745-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="89745-300">เพิ่มการทดสอบที่บันทึกไปยัง Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="89745-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="89745-301">เปิดสภาพแวดล้อม Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="89745-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="89745-302">เลือกโครงการที่คุณกำหนดในพารามิเตอร์ RSAT เมื่อคุณ [ตั้งค่าคอนฟิกเครื่องมือ](#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="89745-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="89745-303">เลือกแผนทดสอบที่คุณกำหนดในพารามิเตอร์ RSAT เมื่อคุณ [ตั้งค่าคอนฟิกเครื่องมือ](#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="89745-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="89745-304">สร้างกรณีทดสอบใหม่สำหรับแผนทดสอบที่เลือก:</span><span class="sxs-lookup"><span data-stu-id="89745-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="89745-305">ตั้งชื่อแผนทดสอบ **จัดเตรียมข้อมูลเพื่อทดสอบการประมวลผลของการชำระเงินทางอิเล็กทรอนิกส์ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="89745-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="89745-306">แนบไฟล์ **Recording.xml** จากโฟลเดอร์ **จัดเตรียม** ที่คุณดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="89745-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="89745-307">สร้างกรณีทดสอบใหม่สำหรับแผนทดสอบที่เลือก:</span><span class="sxs-lookup"><span data-stu-id="89745-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="89745-308">ตั้งชื่อแผนทดสอบ **การประมวลผลการทดสอบของการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้ BACS (UK) รูปแบบ ER**</span><span class="sxs-lookup"><span data-stu-id="89745-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="89745-309">แนบไฟล์ **Recording.xml** จากโฟลเดอร์ **ประมวลผล** ที่คุณดาวน์โหลดมาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="89745-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="89745-310">![กรณีทดสอบใหม่สำหรับแผนทดสอบที่เลือก](media/GER-RSAT-DevOps-Tests-Passed.png "ภาพหน้าจอของกรณีทดสอบใหม่สำหรับแผนทดสอบที่เลือก")</span><span class="sxs-lookup"><span data-stu-id="89745-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="89745-311">ให้ความสำคัญกับลำดับการดำเนินการที่ถูกต้องของการทดสอบที่ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="89745-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="89745-312">จัดเตรียม RSAT เพื่อรันการทดสอบที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="89745-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="89745-313">โหลดการทดสอบจาก Azure DevOps ไปยัง RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="89745-314">เปิดแอพลิเคชันของ RSAT เฉพาะที่ในโทโพโลยีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="89745-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="89745-315">เลือก **โหลด** เพื่อโหลดการทดสอบที่ขณะนี้อยู่ใน Azure DevOps ลงใน RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="89745-316">![การทดสอบที่โหลดไปยัง RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "ภาพหน้าจอของการทดสอบที่โหลดลงใน RSAT")</span><span class="sxs-lookup"><span data-stu-id="89745-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="89745-317">สร้างไฟล์ระบบอัตโนมัติและพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="89745-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="89745-318">ใน RSAT เลือกการทดสอบที่คุณโหลดจาก Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="89745-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="89745-319">เลือก **สร้าง** เพื่อสร้างไฟล์ระบบอัตโนมัติและพารามิเตอร์ของ RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="89745-320">![ไฟล์ระบบอัตโนมัติและพารามิเตอร์ RSAT ที่สร้างใน RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "ภาพหน้าจอของไฟล์ระบบอัตโนมัติและพารามิเตอร์ RSAT ที่สร้างใน RSAT")</span><span class="sxs-lookup"><span data-stu-id="89745-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="89745-321">ปรับเปลี่ยนไฟล์พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="89745-321">Modify the parameters files</span></span>

1. <span data-ttu-id="89745-322">ใน RSAT เลือกกรณีทดสอบ **จัดเตรียมข้อมูลเพื่อทดสอบการประมวลผลของการชำระเงินทางอิเล็กทรอนิกส์ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="89745-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="89745-323">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="89745-323">Select **Edit**.</span></span>
3. <span data-ttu-id="89745-324">ในสมุดงาน Microsoft Excel ที่เปิดอยู่ บนแผ่นงาน **ทั่วไป** ให้เปลี่ยนรหัสบริษัทเป็น **GBSI** เนื่องจากบริษัทนี้จะใช้สำหรับการดำเนินการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="89745-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="89745-325">ใน RSAT เลือกกรณีทดสอบของ **การประมวลผลการทดสอบของการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้ BACS (UK) รูปแบบ ER**</span><span class="sxs-lookup"><span data-stu-id="89745-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="89745-326">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="89745-326">Select **Edit**.</span></span>
6. <span data-ttu-id="89745-327">ในสมุดงาน Excel ที่เปิดอยู่ บนแผ่นงาน **ทั่วไป** ให้เปลี่ยนรหัสบริษัทเป็น **GBSI**</span><span class="sxs-lookup"><span data-stu-id="89745-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="89745-328">บนแผ่นงาน **ERFormatMappingRunLogTable** ให้สังเกตว่าเซลล์ A:3 และ C:3 มีข้อความของฟิลด์ในตารางล็อกดีบัก ER ที่ใช้เพื่อตรวจสอบความถูกต้องของผลลัพธ์ของการเปรียบเทียบเอาท์พุทกับข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="89745-329">ข้อความเหล่านี้จะใช้ในการประเมินเรกคอร์ดของล็อกดีบัก ER ซึ่งสร้างขึ้นในระหว่างการดำเนินการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="89745-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="89745-330">![แผ่นงาน ERFormatMappingRunLogTable](media/GER-RSAT-RSAT-ExcelParameters.png "ภาพหน้าจอของแผ่นงาน ERFormatMappingRunLogTable")</span><span class="sxs-lookup"><span data-stu-id="89745-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="89745-331">รันการทดสอบและวิเคราะห์ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="89745-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="89745-332">รันการทดสอบใน RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="89745-333">ใน RSAT เลือกการทดสอบที่โหลด</span><span class="sxs-lookup"><span data-stu-id="89745-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="89745-334">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="89745-334">Select **Run**.</span></span>

<span data-ttu-id="89745-335">โปรดสังเกตว่ากรณีทดสอบจะรันโดยอัตโนมัติในแอพลิเคชั่น โดยใช้เว็บเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="89745-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="89745-336">วิเคราะห์ผลลัพธ์ของการดำเนินการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="89745-336">Analyze the results of test execution</span></span>

<span data-ttu-id="89745-337">ผลลัพธ์ของการดำเนินการทดสอบจะถูกจัดเก็บไว้ใน RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="89745-338">โปรดสังเกตว่ามีการส่งผ่านการทดสอบทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="89745-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="89745-339">![การทดสอบที่ส่งผ่านใน RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "ภาพหน้าจอของการทดสอบที่ส่งผ่านใน RSAT")</span><span class="sxs-lookup"><span data-stu-id="89745-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="89745-340">โปรดสังเกตว่าผลลัพธ์ของการดำเนินการทดสอบจะถูกส่งไปยัง Azure DevOps ด้วย เพื่อให้คุณสามารถทำการวิเคราะห์เพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="89745-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="89745-341">![ผลลัพธ์ของการดำเนินการทดสอบใน Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "ภาพหน้าจอของผลลัพธ์ของการดำเนินการทดสอบใน Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="89745-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="89745-342">จำลองสถานการณ์ที่ซึ่งการทดสอบล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="89745-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="89745-343">ชุดการทดสอบนี้ต้องล้มเหลว เมื่อเอาท์พุทที่สร้างขึ้นอย่างน้อยหนึ่งรายการไม่ตรงกับพื้นฐานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="89745-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="89745-344">เมื่อต้องการให้บรรลุสถานการณ์นี้ คุณสามารถใช้รุ่นที่ได้รับของรูปแบบ **BACS (UK)** ของคุณ ซึ่งจะสร้างไฟล์การชำระเงินที่มีเนื้อหาที่แตกต่างจากข้อมูลพื้นฐานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="89745-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="89745-345">เมื่อต้องการจำลองสถานการณ์นี้ คุณสามารถใช้รูปแบบ **BACS (UK)** เดียวกัน แต่เปลี่ยนยอดการชำระเงินในรายการการชำระเงินที่ประมวลผลแล้ว</span><span class="sxs-lookup"><span data-stu-id="89745-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="89745-346">เปิดแอพลิเคชั่น แล้วไปยัง **บัญชีเจ้าหนี้ \> การชำระเงิน \> สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="89745-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="89745-347">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="89745-347">Select **Lines**.</span></span>
3. <span data-ttu-id="89745-348">เลือกรายการการชำระเงิน แล้วเลือก **สถานะการชำระเงิน \> ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="89745-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="89745-349">ในฟิลด์ **เดบิต** เปลี่ยนค่าจาก **1,000.00** เป็น **2,000.00**</span><span class="sxs-lookup"><span data-stu-id="89745-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="89745-350">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="89745-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="89745-351">รันการทดสอบใน RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="89745-352">ใน RSAT เลือกการทดสอบที่โหลด</span><span class="sxs-lookup"><span data-stu-id="89745-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="89745-353">เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="89745-353">Select **Run**.</span></span>

<span data-ttu-id="89745-354">โปรดสังเกตว่ากรณีทดสอบจะรันโดยอัตโนมัติในแอพลิเคชั่น โดยใช้เว็บเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="89745-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="89745-355">วิเคราะห์ผลลัพธ์ของการดำเนินการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="89745-355">Analyze the results of test execution</span></span>

<span data-ttu-id="89745-356">ผลลัพธ์ของการดำเนินการทดสอบจะถูกจัดเก็บไว้ใน RSAT</span><span class="sxs-lookup"><span data-stu-id="89745-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="89745-357">โปรดสังเกตว่าการทดสอบที่สองล้มเหลวในระหว่างการดำเนินการที่สอง</span><span class="sxs-lookup"><span data-stu-id="89745-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="89745-358">![ผลการทดสอบที่ล้มเหลวใน RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "ภาพหน้าจอของผลการทดสอบที่ล้มเหลวใน RSAT")</span><span class="sxs-lookup"><span data-stu-id="89745-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="89745-359">โปรดสังเกตว่าผลลัพธ์ของการดำเนินการทดสอบจะถูกส่งไปยัง Azure DevOps ด้วย เพื่อให้คุณสามารถทำการวิเคราะห์เพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="89745-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="89745-360">![ผลการทดสอบที่ล้มเหลวใน Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "ภาพหน้าจอของผลการทดสอบที่ล้มเหลวใน Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="89745-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="89745-361">คุณสามารถเข้าถึงสถานะของการทดสอบแต่ละครั้งได้</span><span class="sxs-lookup"><span data-stu-id="89745-361">You can access the status of each test.</span></span> <span data-ttu-id="89745-362">นอกจากนี้ คุณยังสามารถเข้าถึงล็อกการดำเนินการเพื่อให้คุณวิเคราะห์เหตุผลสำหรับความล้มเหลวใดๆ</span><span class="sxs-lookup"><span data-stu-id="89745-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="89745-363">ในภาพประกอบต่อไปนี้ ล็อกการดำเนินการแสดงว่าความล้มเหลวเกิดขึ้น เนื่องจากความแตกต่างในเนื้อหาระหว่างไฟล์การชำระเงินที่สร้างขึ้นและข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="89745-364">![ล็อกการดำเนินการสำหรับการวิเคราะห์ความล้มเหลวใน Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "ภาพหน้าจอของล็อกการดำเนินการสำหรับการวิเคราะห์ล้มเหลวใน Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="89745-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="89745-365">ดังนั้น ดังที่คุณได้เห็น สามารถมีการประเมินการทำงานของรูปแบบ ER ใดๆ ได้โดยอัตโนมัติ โดยใช้ RSAT เป็นแพลตฟอร์มการทดสอบ และโดยใช้กรณีทดสอบที่ยึดตามตัวบันทึกงานซึ่งใช้คุณลักษณะพื้นฐานของ ER</span><span class="sxs-lookup"><span data-stu-id="89745-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89745-366">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="89745-366">Additional resources</span></span>

- [<span data-ttu-id="89745-367">ทรัพยากรตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="89745-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="89745-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="89745-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="89745-369">สร้างและดำเนินการทดสอบการยอมรับของผู้ใช้อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="89745-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="89745-370">ปรับใช้และใช้สภาพแวดล้อมที่รองรับระบบอัตโนมัติของบิลด์และการทดสอบแบบต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="89745-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="89745-371">ติดตามผลของรายงานที่จัดทำและเปรียบเทียบผลกับค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="89745-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="89745-372">ER อัพเกรดรูปแบบของคุณโดยการใช้เวอร์ชันฐานใหม่ของรูปแบบนั้น</span><span class="sxs-lookup"><span data-stu-id="89745-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="89745-373">ER นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="89745-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)
