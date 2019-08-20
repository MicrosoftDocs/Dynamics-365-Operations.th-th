---
title: ตั้งค่าและติดตั้งบทช่วยสอนของ Regression Suite Automation Tool
description: หัวข้อนี้เป็นบทช่วยสอนที่แสดงวิธีการตั้งค่าและติดตั้ง Regression Suite Automation Tool (RSAT)
author: kfend
manager: AnnBe
ms.date: 06/24/2019
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
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: e2287cb0281e920de219cb88d41cd69264911f93
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850883"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="212be-103">ตั้งค่าและติดตั้งบทช่วยสอนของ Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="212be-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="212be-104">หัวข้อนี้เป็นบทช่วยสอนที่ช่วยให้คุณได้รับการตั้งค่าและเริ่มต้นด้วย RSAT และเครื่องมือที่เกี่ยวข้องกับการใช้ RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="212be-105">ใช้เครื่องมือเบราว์เซอร์อินเทอร์เน็ตของคุณเพื่อดาวน์โหลดและบันทึกหน้านี้ในรูปแบบ PDF</span><span class="sxs-lookup"><span data-stu-id="212be-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="212be-106">แนวคิดหลัก</span><span class="sxs-lookup"><span data-stu-id="212be-106">Key concepts</span></span>

- <span data-ttu-id="212be-107">ทำความเข้าใจการตั้งค่าของการติดตั้งและข้อกำหนดเบื้องต้นที่จำเป็นสำหรับแอพลิเคชันต่างๆ ที่สนับสนุน Regression Suite Automation Tool (RSAT)</span><span class="sxs-lookup"><span data-stu-id="212be-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="212be-108">ทำความเข้าใจวิธีที่คุณลักษณะตัวบันทึกงานใน Microsoft Dynamics 365 for Finance and Operations พร้อมด้วย Microsoft Dynamics Lifecycle Services (LCS) และ Microsoft Azure DevOps อนุญาตให้คุณสามารถสร้าง ตั้งค่าคอนฟิก รัน ตรวจสอบ และรายงานเกี่ยวกับกรณีทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-108">Understand how the Task recorder feature in Microsoft Dynamics 365 for Finance and Operations, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="212be-109">เพิ่มประสิทธิภาพผู้ใช้งานตามหน้าที่ให้สามารถบันทึกงานธุรกิจได้โดยใช้ตัวบันทึกงานใน Finance and Operations แล้วจากนั้น แปลงการบันทึกงานลงในชุดของการทดสอบแบบอัตโนมัติโดยไม่ต้องเขียนรหัสต้นทาง</span><span class="sxs-lookup"><span data-stu-id="212be-109">Empower functional users to record business tasks by using Task recorder in Finance and Operations, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="212be-110">ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="212be-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="212be-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="212be-111">Prerequisites</span></span>

- <span data-ttu-id="212be-112">สภาพแวดล้อม Finance and Operations ที่รัน Microsoft Dynamics 365 for Finance and Operations รุ่น 10.0 (เมษายน 2019) หรือรุ่นที่ใหม่กว่า จำเป็นสำหรับบทช่วยสอนนี้</span><span class="sxs-lookup"><span data-stu-id="212be-112">A Finance and Operations environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="212be-113">สำหรับลูกค้าที่ใช้ Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3 การปรับปรุงแพลตฟอร์ม 20 (PU20) หรือใหม่กว่า ยังได้รับการสนับสนุนด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="212be-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="212be-114">ผู้ใช้ต้องมีสิทธิ์ของผู้ดูแลระบบในการเข้าถึงสภาพแวดล้อม Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-114">The user must have admin rights to the Finance and Operations environment.</span></span>
- <span data-ttu-id="212be-115">คุณต้องมีสิทธิเข้าถึงผู้เช่าของลูกค้า LCS และ Azure DevOps (ก่อนหน้านี้เรียกว่า Microsoft Visual Studio Team Services \[VSTS\])</span><span class="sxs-lookup"><span data-stu-id="212be-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="212be-116">ผู้ใช้ที่กำลังสร้างและจัดการชุดทดสอบต้องมีสิทธิ์การใช้งาน Test Plans หรือ Test Manager ของ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="212be-117">นอกจากนี้ สิทธิ์การใช้งานต่อไปนี้ยังช่วยให้คุณสามารถเข้าถึง Test Plans:</span><span class="sxs-lookup"><span data-stu-id="212be-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="212be-118">ลิขสิทธิ์ Visual Studio Enterprise</span><span class="sxs-lookup"><span data-stu-id="212be-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="212be-119">ลิขสิทธิ์ Visual Studio Test Professional</span><span class="sxs-lookup"><span data-stu-id="212be-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="212be-120">สิทธิ์การใช้งานของสมาชิกของแพลตฟอร์ม MSDN</span><span class="sxs-lookup"><span data-stu-id="212be-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="212be-121">RSAT ต้องมีสิทธิ์เข้าถึงสภาพแวดล้อมการทดสอบผ่านทางเว็บเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="212be-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="212be-122">เมื่อต้องการสร้างและแก้ไขพารามิเตอร์การทดสอบ คุณต้องติดตั้ง Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="212be-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="212be-123">ตั้งค่าคอนฟิก Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="212be-124">การมีสิทธิ์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="212be-124">User eligibility</span></span>

<span data-ttu-id="212be-125">ตรวจสอบให้แน่ใจว่ามีการสร้างผู้ใช้ใน Azure DevOps และมีระดับการบอกรับเป็นสมาชิกที่ให้สิทธิ์เข้าถึง Azure Test Plans</span><span class="sxs-lookup"><span data-stu-id="212be-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="212be-126">ต้องมีสิทธิ์การใช้งาน Azure DevOps Test Plans เฉพาะเมื่อผู้ใช้จะสร้างและจัดการกรณีการทดสอบ (กล่าวคือ ไม่ใช่ผู้ใช้ RSAT ทั้งหมดต้องมีสิทธิ์การใช้งานนี้)</span><span class="sxs-lookup"><span data-stu-id="212be-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="212be-127">สำหรับข้อมูลเกี่ยวกับข้อกำหนดสิทธิ์การใช้งาน โปรดดู [ข้อกำหนดสิทธิ์การใช้งาน](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements)</span><span class="sxs-lookup"><span data-stu-id="212be-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="212be-128">สร้างโครงการ Azure DevOps ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="212be-129">RSAT ใช้ Azure Devops สำหรับกรณีทดสอบและการจัดการชุดทดสอบ การรายงาน และการตรวจสอบผลลัพธ์การรันการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="212be-130">คุณสามารถใช้โครงการ Azure DevOps ที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="212be-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="212be-131">อย่างไรก็ตาม ถ้ามีการตั้งค่าโครงการ Azure DevOps ที่มีอยู่ของคุณเพื่อให้มีเท็มเพลตที่กำหนดเอง คุณจะได้รับข้อผิดพลาด "ความล้มเหลวในการซิงค์กับ VSTS" เมื่อคุณซิงค์กรณีทดสอบจากตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM) กับ Azure DevOps (ดูส่วน [ทดสอบการซิงโครไนส์จาก BPM ไปยัง Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) )</span><span class="sxs-lookup"><span data-stu-id="212be-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="212be-132">ถ้ามีการปฏิบัติตามแนวทางที่พึงปฏิบัติต่อไปนี้สำหรับเท็มเพลตที่กำหนดเอง คุณจะสามารถซิงค์กรณีการทดสอบกับ Azure DevOps ได้</span><span class="sxs-lookup"><span data-stu-id="212be-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="212be-133">(แนวทางที่พึงปฏิบัติเหล่านี้จะแสดงรายการอยู่ในข้อความแสดงข้อผิดพลาด)</span><span class="sxs-lookup"><span data-stu-id="212be-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="212be-134">อย่าลบชนิดรายการงานหรือฟิลด์แบบสำเร็จรูปใดๆ</span><span class="sxs-lookup"><span data-stu-id="212be-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="212be-135">อย่าลบสถานะของชนิดรายการงานใดๆ</span><span class="sxs-lookup"><span data-stu-id="212be-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="212be-136">อย่าเพิ่มฟิลด์ที่จำเป็นใดๆ ไปยังชนิดรายการงาน</span><span class="sxs-lookup"><span data-stu-id="212be-136">Do not add any required fields to a work item type.</span></span>

![ข้อความแสดงข้อผิดพลาดที่มีรายการของแนวทางที่พึงปฏิบัติ](./media/setup_rsa_tool_02.png)

<span data-ttu-id="212be-138">มิฉะนั้น สำหรับบทช่วยสอนนี้ เราขอแนะนำให้คุณสร้างโครงการ Azure DevOps ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="212be-139">สำหรับข้อมูลเพิ่มเติม ดู [ปัญหาเมื่อซิงค์กับ BPM โดยใช้เท็มเพลตการประมวลผล Azure DevOps (VSTS) แบบกำหนดเอง](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/)</span><span class="sxs-lookup"><span data-stu-id="212be-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="212be-140">เปิด Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`)</span><span class="sxs-lookup"><span data-stu-id="212be-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="212be-141">เลือก **สร้างโครงการ** ที่มุมขวาบนของหน้า Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![สร้างปุ่มโครงการ](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="212be-143">กรอกข้อมูลในฟิลด์ต่อไปนี้ แล้วเลือก **สร้าง**:</span><span class="sxs-lookup"><span data-stu-id="212be-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="212be-144">**ชื่อโครงการ**</span><span class="sxs-lookup"><span data-stu-id="212be-144">**Project name**</span></span>
    - <span data-ttu-id="212be-145">**การควบคุมรุ่น** – เลือก **Team Foundation Version Control**</span><span class="sxs-lookup"><span data-stu-id="212be-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="212be-146">โปรดทราบว่าตัวเลือกเริ่มต้น **Git** ไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="212be-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="212be-147">**กระบวนการรายการงาน**</span><span class="sxs-lookup"><span data-stu-id="212be-147">**Work item process**</span></span>

    ![กล่องโต้ตอบสร้างโครงการใหม่](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="212be-149">สร้างโทเคนการเข้าถึงส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="212be-149">Create a personal access token</span></span>

<span data-ttu-id="212be-150">ในบทช่วยสอนนี้ คุณจะใช้ LCS Business Process Modeler (BPM) เพื่อสร้างไลบรารีกรณีทดสอบ และซิงโครไนส์กรณีการทดสอบของคุณกับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="212be-151">คุณจะต้องใช้โทเคนการเข้าถึงส่วนบุคคลเพื่อซิงค์ BPM กับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="212be-152">เลือกไอคอนโพรไฟล์ที่มุมด้านขวาบนของหน้าสำหรับโครงการ Azure DevOps ของคุณ แล้วเลือก **ความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="212be-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![คำสั่งรักษาความปลอดภัย](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="212be-154">ในบานหน้าต่างด้านซ้าย ภายใต้ **ความปลอดภัย** เลือก **โทเคนการเข้าถึงส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="212be-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="212be-155">จากนั้น เลือก **โทเคนใหม่**</span><span class="sxs-lookup"><span data-stu-id="212be-155">Then select **New Token**.</span></span>

    ![ปุ่มโทเคนใหม่บนแท็บโทเคนการเข้าถึงส่วนบุคคลในการตั้งค่าผู้ใช้](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="212be-157">กรอกข้อมูลในฟิลด์ต่อไปนี้ แล้วเลือก **สร้าง**:</span><span class="sxs-lookup"><span data-stu-id="212be-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="212be-158">**ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="212be-158">**Name**</span></span>
    - <span data-ttu-id="212be-159">**การหมดอายุ (UTC)** – เลือก **กำหนดการกำหนดเองแล้ว** และจากนั้น ใช้ตัวเลือกวันที่เพื่อเลือกวันที่พร้อมใช้งานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="212be-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="212be-160">**ขอบเขต** – เลือกตัวเลือก **การเข้าถึงแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="212be-160">**Scopes** – Select the **Full access** option.</span></span>

    ![กล่องโต้ตอบสร้างโทเคนการเข้าถึงส่วนบุคคลใหม่](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="212be-162">จดบันทึกโทเคนการเข้าถึงส่วนบุคคลที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="212be-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="212be-163">คุณจะต้องใช้ในภายหลัง เมื่อคุณตั้งค่าการตั้งค่าคอนฟิก RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![โทเคนการเข้าถึงส่วนบุคคล](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="212be-165">ตั้งค่าคอนฟิกโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="212be-165">Configure the LCS project</span></span>

<span data-ttu-id="212be-166">คุณต้องมีโครงการ Lifecycle Services (LCS) สำหรับไลบรารีการทดสอบหลักของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="212be-167">LCS Business Process Modeler (BPM) ถูกใช้เป็นไลบรารีหลักสำหรับกรณีทดสอบของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="212be-168">BPM ใช้ในการจัดการและเผยแพร่ไลบรารีการทดสอบในโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="212be-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="212be-169">ตัวอย่างเช่น คู่ค้า Microsoft หรือผู้จัดจำหน่ายซอฟต์แวร์อิสระ (ISV) ซึ่งสร้างไลบรารีการทดสอบ จะนำกรณีทดสอบออกใช้ในรูปแบบของไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="212be-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="212be-170">ใน BPM กรณีทดสอบจะถูกจัดระเบียบตามกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="212be-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="212be-171">BPM ไม่ได้กำหนดลำดับการดำเนินการหรือความถี่ของการผ่านการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="212be-172">รายละเอียดเหล่านี้จะถูกจัดการใน Azure DevOps ตามที่อธิบายไว้ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="212be-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="212be-173">สำหรับโครงการ LCS ของคุณ คุณสามารถใช้การดำเนินงานของลูกค้าที่มีอยู่ หรือโครงการคู่ค้า</span><span class="sxs-lookup"><span data-stu-id="212be-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="212be-174">ปรับปรุงภาษา LCS</span><span class="sxs-lookup"><span data-stu-id="212be-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="212be-175">สำหรับอินเทอร์เฟสผู้ใช้ (UI) เพื่อแสดงกระบวนการทางธุรกิจอย่างถูกต้อง ต้องตั้งค่าภาษาที่ต้องการ LCS เป็น **ภาษาอังกฤษ (สหรัฐอเมริกา)**</span><span class="sxs-lookup"><span data-stu-id="212be-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="212be-176">ไปที่โครงการสำหรับการใช้งาน LCS</span><span class="sxs-lookup"><span data-stu-id="212be-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="212be-177">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ในมุมขวาบน และจากนั้น เลือก **การกำหนดลักษณะภาษา**</span><span class="sxs-lookup"><span data-stu-id="212be-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![คำสั่งบนเมนูการตั้งค่า](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="212be-179">ในฟิลด์ **การกำหนดลักษณะภาษา** เลือก **ภาษาอังกฤษ (สหรัฐอเมริกา)** แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![แท็บการกำหนดลักษณะภาษาในการตั้งค่าผู้ใช้](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="212be-181">ตั้งค่าคอนฟิก LCS เพื่อเชื่อมต่อกับโครงการ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="212be-182">ถ้าคุณสร้างโครงการ Azure DevOps ใหม่ก่อนหน้านี้ ให้ตั้งค่าคอนฟิกโครงการ LCS เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="212be-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="212be-183">มิฉะนั้น ถ้าโครงการ LCS ของคุณเชื่อมต่อกับโครงการ Azure DevOps ของคุณอยู่แล้ว คุณสามารถดำเนินการต่อไปยังส่วนถัดไปได้</span><span class="sxs-lookup"><span data-stu-id="212be-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="212be-184">ไปที่โครงการสำหรับการใช้งาน LCS</span><span class="sxs-lookup"><span data-stu-id="212be-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="212be-185">เลือกปุ่ม **เมนู** แล้วจากนั้น เลือก **การตั้งค่าโครงการ**</span><span class="sxs-lookup"><span data-stu-id="212be-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![คำสั่งการตั้งค่าโครงการ](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="212be-187">ในบานหน้าต่างด้านซ้าย ให้เลือก **Visual Studio Team Services** แล้วจากนั้น เลือก **ตั้งค่า Visual Studio Team Services**</span><span class="sxs-lookup"><span data-stu-id="212be-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![แท็บ Visual Studio Team Services ในการตั้งค่าโครงการ](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="212be-189">ในฟิลด์ **URL ของไซต์ Azure DevOps** ให้ป้อน URL ของไซต์ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="212be-190">ในฟิลด์ **โทเคนการเข้าถึงส่วนบุคคล** ให้ป้อนโทเคนการเข้าถึงส่วนบุคคลที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="212be-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-191">ถึงแม้ว่าขณะนี้ VSTS ถูกเรียกว่า Azure DevOps เพื่อเชื่อมต่อ LCS กับโครงการ Azure DevOps ของคุณ ให้ใช้ URL เก่า</span><span class="sxs-lookup"><span data-stu-id="212be-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="212be-192">ตัวอย่างเช่น URL ของ Azure DevOps ที่ใช้ในบทช่วยสอนนี้คือ `https://dev.azure.com/D365FOFastTrack/`</span><span class="sxs-lookup"><span data-stu-id="212be-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="212be-193">อย่างไรก็ตาม ในภาพประกอบต่อไปนี้ จะมีการป้อนเป็น `https://D365FOFastTrack.visualstudio.com/`</span><span class="sxs-lookup"><span data-stu-id="212be-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![ขั้นตอนที่ 1 ตั้งค่า Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="212be-195">เลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="212be-195">Select **Continue**.</span></span>
6. <span data-ttu-id="212be-196">ในฟิลด์ **โครงการ Visual Studio Team Services** เลือกโครงการ VSTS ในไซต์ที่เลือกเพื่อเชื่อมโยงกับโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="212be-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="212be-197">ฟิลด์ **เท็มเพลตการประมวลผล** ถูกตั้งค่าเป็น **Agile** โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="212be-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="212be-198">สำหรับเท็มเพลตที่กำหนดเอง ให้ทบทวนแนวทางปฏิบัติที่ดีที่สุดในส่วน [สร้างโครงการ Azure DevOps ใหม่](#create-a-new-azure-devops-project)</span><span class="sxs-lookup"><span data-stu-id="212be-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="212be-199">จากนั้น เลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="212be-199">Then select **Continue**.</span></span>

    ![ขั้นตอนที่ 2 ใน ตั้งค่า Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="212be-201">ตรวจทานการตั้งค่าของคุณ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-201">Review your settings, and then select **Save**.</span></span>

    ![ขั้นตอนที่ 3 ใน ตั้งค่า Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="212be-203">เลือก **อนุญาต** เพื่ออนุมัติให้ LCS สามารถเข้าถึงไซต์ Azure DevOps ที่ตั้งค่าคอนฟิกในนามของคุณ และเพื่อเปิดใช้งานคุณลักษณะที่รวมกับ VSTS</span><span class="sxs-lookup"><span data-stu-id="212be-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![อนุมัติปุ่ม](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="212be-205">กล่องข้อความปรากฏขึ้น ซึ่งกล่าวว่า "คุณกำลังจะเปลี่ยนเส้นทางไปยังไซต์ภายนอกเพื่ออนุมัติให้ LCS เชื่อมต่อกับ Visual Studio Team Services ในนามของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="212be-206">ดำเนินการหรือไม่?"</span><span class="sxs-lookup"><span data-stu-id="212be-206">Proceed?"</span></span> <span data-ttu-id="212be-207">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="212be-207">Select **Yes**.</span></span>

    ![กล่องข้อความ](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="212be-209">เลือก **ยอมรับ**</span><span class="sxs-lookup"><span data-stu-id="212be-209">Select **Accept**.</span></span>

    ![การอนุมัติการเข้าถึง](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="212be-211">ถ้าคุณได้รับอนุญาตให้เป็นผู้ใช้ UI ควรคุณกลับไปที่หน้าการตั้งค่าโครงการ LCS</span><span class="sxs-lookup"><span data-stu-id="212be-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![ผู้ใช้ที่ได้รับอนุมัติ](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="212be-213">สร้างไลบรารี BPM ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-213">Create a new BPM library</span></span>

1. <span data-ttu-id="212be-214">ไปที่โครงการสำหรับการใช้งาน LCS</span><span class="sxs-lookup"><span data-stu-id="212be-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="212be-215">เลือกปุ่ม **เมนู** แล้วจากนั้น เลือก **ตัวทำแบบจำลองกระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="212be-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![คำสั่งของตัวทำแบบจำลองกระบวนการทางธุรกิจ](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="212be-217">เลือก **ไลบรารีใหม่**</span><span class="sxs-lookup"><span data-stu-id="212be-217">Select **New library**.</span></span>

    ![ปุ่มไลบรารีใหม่](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="212be-219">ในฟิลด์ **ชื่อไลบรารี** ให้ป้อนชื่อ แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="212be-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="212be-220">สำหรับบทช่วยสอนนี้ ให้ตั้งชื่อในไลบรารี BPM เป็น **RSAT**</span><span class="sxs-lookup"><span data-stu-id="212be-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![กล่องโต้ตอบสร้างไลบรารีใหม่](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="212be-222">เปิดไลบรารี BPM ของ **RSAT** ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="212be-223">เลือกกระบวนการ **กระบวนการทางธุรกิจหลักของตัวอย่าง** และจากนั้น ทางด้านขวา ให้เลือก **โหมดแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="212be-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![ปุ่มแก้ไขโหมด](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="212be-225">เปลี่ยนค่าของทั้งฟิลด์ **ชื่อ** และฟิลด์ **คำอธิบาย** เพื่อ **สร้างผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="212be-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="212be-226">จากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-226">Then select **Save**.</span></span>

    ![ฟิลด์ชื่อและคำอธิบาย](./media/setup_rsa_tool_24.png)

## <a name="finance-and-operations-environment"></a><span data-ttu-id="212be-228">สภาพแวดล้อม Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-228">Finance and Operations environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="212be-229">ข้อกำหนดรุ่น</span><span class="sxs-lookup"><span data-stu-id="212be-229">Version requirement</span></span>

<span data-ttu-id="212be-230">ต้องใช้การทดสอบ Finance and Operations หรือสภาพแวดล้อม sandbox ที่รันรุ่น 10</span><span class="sxs-lookup"><span data-stu-id="212be-230">A Finance and Operations test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="212be-231">สำหรับลูกค้าที่ใช้รุ่น 7.3 การปรับปรุงแพลตฟอร์ม 20 หรือใหม่กว่า ยังได้รับการสนับสนุนด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="212be-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="212be-232">RSAT ต้องมีสิทธิ์เข้าถึงสภาพแวดล้อมการทดสอบ Finance and Operations ของคุณ ผ่านทางเว็บเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="212be-232">RSAT must have access to your Finance and Operations test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="212be-233">เงื่อนไขผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="212be-233">User criteria</span></span>

<span data-ttu-id="212be-234">ผู้ใช้ต้องมีสิทธิ์ของผู้ดูแลระบบสำหรับสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="212be-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="212be-235">ตั้งค่าการตั้งค่าวิธีใช้เพื่อเชื่อมต่อกับ LCS</span><span class="sxs-lookup"><span data-stu-id="212be-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="212be-236">ขั้นตอนนี้จำเป็นต้องใช้ในการเชื่อมต่อกับ LCS เพื่อให้สามารถบันทึกงานที่บันทึกไปยังไลบรารี BPM ที่เหมาะสมใน LCS ผ่านทางไคลเอนต์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the Finance and Operations client.</span></span>

1. <span data-ttu-id="212be-237">เปิดไคลเอนต์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-237">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="212be-238">ไปที่ **การจัดการระบบ \> การตั้งค่า \> พารามิเตอร์ระบบ**</span><span class="sxs-lookup"><span data-stu-id="212be-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="212be-239">บนแท็บ **วิธีใช้** ในฟิลด์ **การตั้งค่าคอนฟิกวิธีใช้ Lifecycle Services** ให้เลือกโครงการ LCS ที่เกี่ยวข้อง (**RSAT** สำหรับบทช่วยสอนนี้)</span><span class="sxs-lookup"><span data-stu-id="212be-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![ฟิลด์การตั้งค่าคอนฟิกวิธีใช้ Lifecycle Services บนแท็บวิธีใช้](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="212be-241">มีการเติมข้อมูลไลบรารี BPM ภายใต้โครงการ LCS ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="212be-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="212be-242">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-242">Select **Save**.</span></span>
5. <span data-ttu-id="212be-243">คุณอาจต้องรีเฟรชเบราว์เซอร์เพื่อดูเนื้อหาวิธีใช้ที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="212be-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![การแจ้งเตือนเกี่ยวกับการรีเฟรชเบราว์เซอร์](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="212be-245">การบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="212be-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="212be-246">ตรวจสอบให้แน่ใจว่าการบันทึกงานทั้งหมดของคุณเริ่มต้นบนแผงควบคุมหลักของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-246">Make sure that all your task recordings start on the main dashboard of Finance and Operations.</span></span> <span data-ttu-id="212be-247">ทำให้การบันทึกแต่ละครั้งสั้น และมุ่งเน้นไปที่งานธุรกิจหนึ่งงาน เช่น การสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="212be-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="212be-248">สร้างการบันทึกงาน และบันทึกไปยังไลบรารี BPM</span><span class="sxs-lookup"><span data-stu-id="212be-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="212be-249">สร้างการบันทึกงานที่สอดคล้องกันที่คุณสามารถแนบกับกระบวนการทางธุรกิจแบบง่ายที่สร้างขึ้นในไลบรารี BPM ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="212be-250">เปิดไคลเอนต์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-250">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="212be-251">บนแดชบอร์ดหลัก เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) แล้วจากนั้น เลือก **ตัวบันทึกงาน**</span><span class="sxs-lookup"><span data-stu-id="212be-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![คำสั่งบนเมนูการตั้งค่า](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="212be-253">เลือก **สร้างการบันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-253">Select **Create recording**.</span></span>

    ![สร้างปุ่มการบันทึก](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="212be-255">กรอกข้อมูลในฟิลด์ **ชื่อของการบันทึก** และ **อธิบายของการบันทึก** และจากนั้น เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="212be-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![ฟิลด์ชื่อของการบันทึกและคำอธิบายของการบันทึก](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="212be-257">บันทึกขั้นตอนสำหรับการสร้างผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="212be-257">Record the steps for creating a product.</span></span> <span data-ttu-id="212be-258">เมื่อเสร็จสิ้นแล้ว ให้เลือก **หยุด** เพื่อหยุดการบันทึก</span><span class="sxs-lookup"><span data-stu-id="212be-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![ขั้นตอนสำหรับการสร้างผลิตภัณฑ์](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="212be-260">เลือก **บันทึกไปยัง Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="212be-260">Select **Save to Lifecycle Services**.</span></span>

    ![ตัวเลือกบันทึก](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="212be-262">ข้อมูลไลบรารีถูกโหลดจาก LCS</span><span class="sxs-lookup"><span data-stu-id="212be-262">Library information is loaded from LCS.</span></span>

    ![ตัวบ่งชี้ความก้าวหน้า](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="212be-264">เลือกไลบรารี BPM เพื่อเชื่อมโยงกับการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="212be-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="212be-265">สำหรับบทช่วยสอนนี้ ให้เลือกไลบรารี BPM ของ **RSAT** ที่สร้างไว้ก่อนหน้านี้ และ **สร้างผลิตภัณฑ์** ที่กระบวนการทางธุรกิจอยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="212be-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="212be-266">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="212be-266">Then select **OK**.</span></span>

    ![การเชื่อมโยงการบันทึกงานกับไลบรารี BPM และกระบวนการทางธุรกิจ](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="212be-268">ข้อความ "การบันทึกไปยัง Lifecycle Services สำเร็จ" ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="212be-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![ข้อความเกี่ยวกับการบันทึกที่สำเร็จไปยัง LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="212be-270">ถ้าคุณต้องการบันทึกการบันทึกงานเฉพาะที่ และจากนั้น อัปโหลดไปยัง BPM ผ่าน LCS ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="212be-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="212be-271">หลังจากเสร็จสิ้นการบันทึก เลือก **บันทึกไปยัง PC นี้**</span><span class="sxs-lookup"><span data-stu-id="212be-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![ตัวเลือกบันทึก](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="212be-273">ในแถบการแจ้งเตือนของเบราว์เซอร์ ให้เลือก **บันทึก** หรือ **บันทึกเป็น** เพื่อบันทึกไฟล์บนคอมพิวเตอร์เฉพาะที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![แถบการแจ้งเตือน](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="212be-275">ไปยังไลบรารี BPM ของ **RSAT** และเลือกกระบวนการทางธุรกิจที่จะบันทึกการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="212be-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="212be-276">บนแท็บ **ภาพรวม** เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="212be-276">On the **Overview** tab, select **Upload**.</span></span>

        ![ปุ่มอัปโหลด](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="212be-278">เลือก **เรียกดู** และเลือกไฟล์ .axtr ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="212be-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="212be-279">จากนั้น เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="212be-279">Then select **Upload**.</span></span>

        ![การเลือกไฟล์ .axtr ที่จะอัปโหลด](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="212be-281">ทดสอบการซิงโครไนส์จาก BPM ไปยัง Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="212be-282">หลังจากที่มีการแนบการบันทึกงานไปยังกระบวนการทางธุรกิจ คุณต้องตรวจสอบว่าสามารถซิงค์กระบวนการทางธุรกิจและการบันทึกงานที่เชื่อมโยงกับ Azure DevOps เป็นคุณลักษณะและกรณีทดสอบได้ (ตามลำดับ) โดยใช้คุณลักษณะของการซิงค์ VSTS ใน LCS</span><span class="sxs-lookup"><span data-stu-id="212be-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="212be-283">ชนิดของรายการงานที่สอดคล้องกันที่สร้างขึ้นใน Azure DevOps จะแตกต่างกันไป โดยขึ้นอยู่กับเท็มเพลตของกระบวนการที่คุณเลือกไว้ เมื่อคุณตั้งค่าคอนฟิกโครงการ LCS ด้วย Azure DevOps ดังที่อธิบายไว้ในส่วน [สร้างโครงการ Azure DevOps ใหม่](#create-a-new-azure-devops-project)</span><span class="sxs-lookup"><span data-stu-id="212be-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="212be-284">ไปยังไลบรารี BPM และเปิดไลบรารี **RSAT** ที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="212be-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="212be-285">เลือกปุ่มจุดไข่ปลา (**...**) และเลือก **การซิงค์ VSTS**</span><span class="sxs-lookup"><span data-stu-id="212be-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![คำสั่งซิงค์ VSTS บนเมนูจุดไข่ปลา](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="212be-287">หลังจากที่ซิงค์ VSTS เสร็จสมบูรณ์แล้ว แท็บ **ข้อกำหนด** จะปรากฏขึ้นทางด้านซ้าย และรวมรายการงาน Azure DevOps ที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="212be-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-288">รายการงานที่สร้างขึ้นใน Azure DevOps จะมีชื่อไลบรารี BPM เป็นคำนำหน้าชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="212be-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![แท็บข้อกำหนด](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="212be-290">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="212be-290">Refresh the page.</span></span>
4. <span data-ttu-id="212be-291">เลือกปุ่มจุดไข่ปลา (**...**) คุณจะเห็นตัวเลือกเพิ่มเติม **ซิงค์กรณีทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="212be-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="212be-292">เลือกตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="212be-292">Select this option.</span></span>

    ![ซิงค์คำสั่งกรณีการทดสอบบนเมนูจุดไข่ปลา](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="212be-294">ถ้าตัวเลือก **ซิงค์กรณีการทดสอบ** ไม่พร้อมใช้งาน หลังจากที่คุณรีเฟรชหน้า ให้ไปที่หน้าหลักสำหรับ BPM และเลือก **ซิงค์กรณีการทดสอบ** สำหรับไลบรารีทั้งหมดเอง</span><span class="sxs-lookup"><span data-stu-id="212be-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="212be-295">ด้วยวิธีนี้ คุณจะบังคับใช้การซิงโครไนส์สำหรับไลบรารีทั้งหมดอย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="212be-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![การเลือกซิงค์กรณีการทดสอบสำหรับไลบรารีทั้งหมด](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="212be-297">หลังจากที่ซิงค์กรณีการทดสอบเสร็จสมบูรณ์ จะมีการสร้างกรณีการทดสอบใหม่บนแท็บ **ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="212be-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![กรณีการทดสอบใหม่บนแท็บความต้องการ](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="212be-299">ไปที่โครงการ Azure DevOps ของคุณ แล้วเลือก **บอร์ด \> รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="212be-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![คำสั่งรายการงานภายใต้บอร์ด](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="212be-301">ตรวจสอบความถูกต้องว่ารายการงานและกรณีการทดสอบที่คุณสร้างขึ้นโดยใช้การซิงโครไนส์ BPM มีอยู่</span><span class="sxs-lookup"><span data-stu-id="212be-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![รายการงานและกรณีทดสอบ](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="212be-303">ติดตั้งและตั้งค่าคอนฟิก RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-303">Install and Configure RSAT</span></span>

<span data-ttu-id="212be-304">RSAT อาจติดตั้งบนคอมพิวเตอร์เครื่องใดก็ได้ที่รัน Windows 10 และสามารถเชื่อมต่อกับสภาพแวดล้อม Finance and Operations ผ่านเว็บเบราเซอร์ (Internet Explorer หรือ Google Chrome)</span><span class="sxs-lookup"><span data-stu-id="212be-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the Finance and Operations environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="212be-305">ก่อนที่คุณจะติดตั้งเครื่องมือรุ่นใหม่ เราขอแนะนำให้คุณถอนการติดตั้งรุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="212be-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="212be-306">ติดตั้งใบรับรองการพิสูจน์ตัวจริง</span><span class="sxs-lookup"><span data-stu-id="212be-306">Install an authentication certificate</span></span>

<span data-ttu-id="212be-307">เมื่อต้องการเปิดใช้งานการรับรองความถูกต้อง คุณต้องสร้างและติดตั้งใบรับรองบนคอมพิวเตอร์เครื่องเดียวกันที่ RSAT กำลังรันอยู่</span><span class="sxs-lookup"><span data-stu-id="212be-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="212be-308">สร้างใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="212be-308">Generate a certificate</span></span>

1. <span data-ttu-id="212be-309">เมื่อต้องการสร้างไฟล์ใบรับรอง ให้เปิดหน้าต่าง Microsoft Windows PowerShell ในฐานะผู้ดูแลระบบ และรันคำสั่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="212be-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="212be-310">เปิดโปรแกรมจัดการใบรับรองโดยป้อน **certlm.msc** ในกล่องโต้ตอบ **รัน** และยืนยันว่าใบรับรอง **D365 ใบรับรองการทดสอบแบบอัตโนมัติ** ถูกสร้างภายใต้ **ส่วนบุคคล \> ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="212be-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-311">ตรวจสอบให้แน่ใจว่าได้ป้อน **certlm.msc** ไม่ใช่ **certmgr.msc** เนื่องจากใบรับรองถูกจัดเก็บอยู่บนคอมพิวเตอร์เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="212be-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![D365 ใบรับรองการทดสอบแบบอัตโนมัติ](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="212be-313">คลิกขวาที่ใบรับรอง แล้วจากนั้น เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="212be-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="212be-314">ไปที่ **หน่วยงานที่ออกใบรับรองหลักที่เชื่อถือได้ \> ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="212be-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![โฟลเดอร์ใบรับรองภายใต้โฟลเดอร์หน่วยงานที่ออกใบรับรองหลักที่เชื่อถือได้](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="212be-316">ในเมนู **การดำเนินการ** ให้เลือก **วาง** เพื่อคัดลอกใบรับรองไปยังสถานที่ **หน่วยงานที่ออกใบรับรองหลักที่เชื่อถือได้**</span><span class="sxs-lookup"><span data-stu-id="212be-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![คำสั่งวางบนเมนูการดำเนินการ](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="212be-318">เมื่อต้องการดูรหัสประจำตัวของใบรับรองที่ติดตั้งไว้ แต่ไม่มีช่องว่างหรืออักขระพิเศษ ให้เปิดหน้าต่าง Windows PowerShell ในฐานะผู้ดูแลระบบ และรันคำสั่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="212be-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="212be-319">บันทึกรหัสประจำตัว เนื่องจากคุณจะต้องใช้ในภายหลัง เมื่อคุณปรับปรุงไฟล์ .wif สำหรับ Application Object Server (AOS) และตั้งค่าการตั้งค่าคอนฟิก RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="212be-320">ตั้งค่าคอนฟิกคอมพิวเตอร์ AOS เพื่อให้ความเชื่อถือในการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="212be-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="212be-321">ถ้าสภาพแวดล้อม Finance and Operations เป็นสภาพแวดล้อมระดับ 2+ รหัสประจำตัวของใบรับรองต้องได้รับการปรับปรุงในไฟล์ wif.config สำหรับคอมพิวเตอร์ AOS **ทั้งหมด** สำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="212be-321">If the Finance and Operations environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="212be-322">สร้างการเชื่อมต่อ Remote Desktop Protocol (RDP) ไปยังคอมพิวเตอร์ AOS</span><span class="sxs-lookup"><span data-stu-id="212be-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="212be-323">รายละเอียดการลงชื่อเข้าใช้จะพร้อมใช้งานในหน้ารายละเอียดของสภาพแวดล้อมใน LCS</span><span class="sxs-lookup"><span data-stu-id="212be-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="212be-324">เปิด Microsoft Internet Information Services (IIS) และค้นหา **AOSService** ในรายการของไซต์</span><span class="sxs-lookup"><span data-stu-id="212be-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService ในรายการของไซต์](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="212be-326">คลิกขวา **สำรวจ** เพื่อเปิดโฟลเดอร์ **\<ไดรฟ์\>: \\AosService\\WebRoot**</span><span class="sxs-lookup"><span data-stu-id="212be-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="212be-327">ค้นหาไฟล์ **wif.config**</span><span class="sxs-lookup"><span data-stu-id="212be-327">Find the **wif.config** file.</span></span>

    ![ไฟล์ Wif.config ในโฟลเดอร์ WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="212be-329">ปรับปรุงไฟล์ **wif.config** โดยการเพิ่มรายการหน่วยงานใหม่สำหรับชื่อใบรับรองและชื่อหน่วยงานของคุณ ดังที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="212be-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="212be-330">ถ้าผู้ใช้หลายรายใช้แอพลิเคชัน Finance and Operations เดียวกัน ผู้ใช้แต่ละรายจะต้องสร้างรหัสประจำตัวที่แยกต่างหาก และต้องมีการเพิ่มรหัสประจำตัวเหล่านั้นแต่ละรหัสในส่วน **\<คีย์\>**</span><span class="sxs-lookup"><span data-stu-id="212be-330">If multiple users are using the same Finance and Operations application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="212be-331">ถ้ามีคอมพิวเตอร์ AOS มากกว่าหนึ่งเครื่อง ให้ทำซ้ำขั้นตอนที่ 3 ถึง 4 สำหรับคอมพิวเตอร์เพิ่มเติมแต่ละเครื่อง</span><span class="sxs-lookup"><span data-stu-id="212be-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-332">แตกต่างจากสภาพแวดล้อมระดับที่ 2 สภาพแวดล้อมระดับที่ 2 ใหม่จะถูกปรับใช้กับอินสแตนซ์ AOS สองรายการ</span><span class="sxs-lookup"><span data-stu-id="212be-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="212be-333">รัน **iisreset** บนคอมพิวเตอร์ AOS ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="212be-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-334">ถ้าคุณไม่มีสิทธิ์ของผู้ดูแลระบบในการรัน **iisreset** บนคอมพิวเตอร์ระดับที่ 1 บนหน้ารายละเอียดสภาพแวดล้อมใน LCS ให้เลือกรักษา > เริ่มต้นบริการอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="212be-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="212be-335">สภาพแวดล้อมระดับ 2+</span><span class="sxs-lookup"><span data-stu-id="212be-335">Tier 2+ environment</span></span>

<span data-ttu-id="212be-336">ถ้ามีการใช้สภาพแวดล้อม Finance and Operations ระดับ 2+ (Sandbox ของการทดสอบการยอมรับระดับมาตรฐาน หรือสูงกว่า) ให้ตรวจสอบหรือตั้งค่าการตั้งค่ารีจิสทรีต่อไปนี้บนคอมพิวเตอร์ที่มีการติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) Finance and Operations environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="212be-337">ขั้นตอนนี้จำเป็น เนื่องจากจะช่วยให้คุณสามารถหลีกเลี่ยงข้อผิดพลาดในการตรวจสอบความถูกต้องหรือการเชื่อมต่อ RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="212be-338">ติดตั้ง RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-338">Install RSAT</span></span>

1. <span data-ttu-id="212be-339">ไปที่ <https://www.microsoft.com/download/details.aspx?id=57357> แล้วเลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="212be-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="212be-340">เลือกไฟล์ทั้งหมด แล้วจากนั้น เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="212be-340">Select all the files, and then select **Next**.</span></span>

    ![การเลือกไฟล์ทั้งหมด](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="212be-342">คลิกสองครั้งที่แพคเกจ .msi เพื่อรันตัวติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="212be-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="212be-343">จากนั้น เมื่อการติดตั้งเสร็จสมบูรณ์ ให้เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="212be-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![ไฟล์ตัวติดตั้ง RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="212be-345">ติดตั้ง Selenium และไดรเวอร์ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="212be-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="212be-346">ในรุ่นก่อนหน้าของ RSAT คุณต้องติดตั้งไดรเวอร์ของ Selenium และเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="212be-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="212be-347">คุณไม่จำเป็นต้องติดตั้งไดรเวอร์เหล่านี้อีกต่อไป เนื่องจากมีการติดตั้งโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="212be-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="212be-348">ในครั้งแรกที่คุณเปิด RSAT คุณจะได้รับพร้อมท์ให้ดาวน์โหลดและติดตั้ง Selenium โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="212be-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="212be-349">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ตั้งค่าคอนฟิก RSAT](#configure-rsat)</span><span class="sxs-lookup"><span data-stu-id="212be-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="212be-350">ก่อนที่คุณจะสามารถรันกรณีการทดสอบ คุณจะได้รับพร้อมท์ให้ดาวน์โหลดและติดตั้งไดรเวอร์ของเบราว์เซอร์ที่สอดคล้องกับเบราว์เซอร์เริ่มต้นที่เลือกไว้ในการตั้งค่าคอนฟิก RSAT โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="212be-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="212be-351">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [โหลดและรันกรณีการทดสอบ](#load-and-run-test-cases)</span><span class="sxs-lookup"><span data-stu-id="212be-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="212be-352">เริ่มต้นใช้งาน RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="212be-353">การสร้างแผนการทดสอบและชุดการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="212be-354">ไปที่โครงการ Azure DevOps และเลือก **แผนการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="212be-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![คำสั่งแผนการทดสอบ](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="212be-356">เลือก **แผนการทดสอบใหม่**</span><span class="sxs-lookup"><span data-stu-id="212be-356">Select **New Test Plan**.</span></span>

    ![ปุ่มแผนการทดสอบใหม่](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="212be-358">กรอกข้อมูลในฟิลด์ **ชื่อ** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="212be-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="212be-359">สำหรับบทช่วยสอนนี้ ตั้งชื่อแผนการทดสอบ **แผนการทดสอบ RSAT**</span><span class="sxs-lookup"><span data-stu-id="212be-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![กล่องโต้ตอบแผนการทดสอบใหม่](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="212be-361">เลือกเครื่องหมายบวก (**+**) แล้วจากนั้น เลือก **ชุดแบบคงที่** เพื่อสร้างชุดแบบคงที่ภายใต้แผนการทดสอบใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="212be-362">ตั้งชื่อชุดการทดสอบใหม่ **T01 – การผลิตตามสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="212be-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-363">นอกจากนี้ คุณยังสามารถสร้างชุดตามแบบสอบถาม ถ้าคุณต้องการกรณีการทดสอบใหม่จาก BPM เพื่อให้ถูกดึงเข้าไปในชุดการทดสอบ RSAT โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="212be-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![การสร้างชุดแบบคงที่](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="212be-365">แนบกรณีการทดสอบไปยังชุดการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="212be-366">เลือก **เพิ่มรายการที่มีอยู่** ทางด้านขวาเพื่อเพิ่มกรณีการทดสอบที่มีอยู่ลงในชุดการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![เพิ่มปุ่มที่มีอยู่](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="212be-368">ในหน้า **เพิ่มกรณีการทดสอบลงในชุด** เลือก **รันการสอบถาม** แล้วจากนั้น เลือกกรณีการทดสอบเพื่อเพิ่มเข้าไปในชุดการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="212be-369">สำหรับบทช่วยสอนนี้ ให้เลือกกรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="212be-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="212be-370">จากนั้น เลือก **เพิ่มกรณีการทดสอบ** ที่มุมขวาล่างของหน้า (ปุ่มนี้จะไม่แสดงในภาพประกอบต่อไปนี้)</span><span class="sxs-lookup"><span data-stu-id="212be-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![รันปุ่มการสอบถาม](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="212be-372">กรณีการทดสอบจะถูกเพิ่มเข้าไปในชุดการทดสอบ **T01-การผลิตตามสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="212be-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![กรณีการทดสอบที่เพิ่มในชุดการทดสอบ](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="212be-374">ตั้งค่าคอนฟิก RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-374">Configure RSAT</span></span>

1. <span data-ttu-id="212be-375">เปิด RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-375">Open RSAT.</span></span>

    ![ไอคอน RSAT](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="212be-377">คุณได้รับข้อความแจ้งเตือนที่ระบุว่า "Regression Suite Automation Tool ต้องมี Selenium คุณต้องการดาวน์โหลดและติดตั้งโดยอัตโนมัติเดี๋ยวนี้หรือไม่?"</span><span class="sxs-lookup"><span data-stu-id="212be-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="212be-378">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="212be-378">Select **Yes**.</span></span>

    ![ข้อความเตือน](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="212be-380">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์รูปเกียร์) ที่มุมขวาบน และจากนั้น ในกล่องโต้ตอบที่ปรากฏขึ้น ให้กรอกข้อมูลในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="212be-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="212be-381">**Url ของ Azure DevOps** – ป้อน URL ของโครงการ Azure DevOps ของคุณ เช่น `https://yourAzureDevOpsUrlHere.visualStudio.com`</span><span class="sxs-lookup"><span data-stu-id="212be-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="212be-382">**โทเคนการเข้าถึง** – ป้อนโทเคนการเข้าถึงซึ่งช่วยให้เครื่องมือสามารถเชื่อมต่อกับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="212be-383">ใช้โทเคนการเข้าถึงส่วนบุคคลที่คุณสร้างไว้ก่อนหน้านี้ในบทช่วยสอนนี้</span><span class="sxs-lookup"><span data-stu-id="212be-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="212be-384">สำหรับข้อมูลเพิ่มเติม ดู [ตรวจสอบสิทธิ์การเข้าถึงโดยใช้โทเคนการเข้าถึงส่วนบุคคล](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate)</span><span class="sxs-lookup"><span data-stu-id="212be-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="212be-385">**ชื่อโครงการ** – เลือกชื่อของโครงการ Azure DevOps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="212be-386">**แผนการทดสอบ** – เลือกแผนการทดสอบ Azure DevOps ที่มีกรณีการทดสอบของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="212be-387">สำหรับข้อมูลเพิ่มเติม ดู [สร้างแผนการทดสอบและชุดการทดสอบ](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan)</span><span class="sxs-lookup"><span data-stu-id="212be-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="212be-388">หลังจากที่คุณเลือกแผนการทดสอบ ให้เลือก **ทดสอบการเชื่อมต่อ** เพื่อทดสอบการเชื่อมต่อของคุณกับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="212be-389">**ชื่อโฮสต์** – ป้อนชื่อโฮสต์ของสภาพแวดล้อมการทดสอบ Finance and Operations เช่น **\<myaos\>.cloudax.dynamics.com**</span><span class="sxs-lookup"><span data-stu-id="212be-389">**Hostname** – Enter the host name of the Finance and Operations test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="212be-390">อย่ารวมคำนำหน้า **https://** หรือ **http://**</span><span class="sxs-lookup"><span data-stu-id="212be-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="212be-391">**ชื่อโฮสต์ SOAP** – ป้อนชื่อโฮสต์ SOAP ของสภาพแวดล้อมการทดสอบ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-391">**SOAP Hostname** – Enter the SOAP host name of the Finance and Operations test environment.</span></span> <span data-ttu-id="212be-392">โดยทั่วไป ชื่อโฮสต์ SOAP จะเหมือนกับชื่อโฮสต์ แต่มีคำต่อท้าย **soap**</span><span class="sxs-lookup"><span data-stu-id="212be-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="212be-393">นี่คือตัวอย่าง **\<myaos\>soap.cloudax.dynamics.com**</span><span class="sxs-lookup"><span data-stu-id="212be-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="212be-394">อย่ารวมคำนำหน้า **https://** หรือ **http://**</span><span class="sxs-lookup"><span data-stu-id="212be-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="212be-395">เมื่อต้องการค้นหาชื่อโฮสต์และชื่อโฮสต์ SOAP ให้เปิดโปรแกรมจัดการ IIS คลิกขวา **ไซต์ \> AOSService** และจากนั้น เลือก **แก้ไขการผูก**</span><span class="sxs-lookup"><span data-stu-id="212be-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="212be-396">ค่าในคอลัมน์ **ชื่อโฮสต์** จะให้ชื่อโฮสต์และชื่อโฮสต์ SOAP (ชื่อโฮสต์ SOAP มีคำต่อท้าย **soap** ใน URL)</span><span class="sxs-lookup"><span data-stu-id="212be-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![ชื่อโฮสต์และชื่อโฮสต์ SOAP ในคอลัมน์ชื่อโฮสต์](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="212be-398">**ชื่อผู้ใช้ที่เป็นผู้ดูแลระบบ** – ป้อนที่อยู่อีเมลของผู้ใช้ที่เป็นผู้ดูแลระบบในสภาพแวดล้อมการทดสอบ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-398">**Admin user name** – Enter the email address of an admin user in the Finance and Operations test environment.</span></span>
    - <span data-ttu-id="212be-399">**รหัสประจำตัว** – ป้อนรหัสประจำตัวของใบรับรองการพิสูจน์ตัวจริง ดังที่อธิบายไว้ก่อนหน้านี้ในบทช่วยสอนนี้</span><span class="sxs-lookup"><span data-stu-id="212be-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="212be-400">**ไดเรกทอรีการทำงาน** – ระบุตำแหน่งโฟลเดอร์สำหรับจัดเก็บไฟล์การทำงานอัตโนมัติของการทดสอบ เช่น ไฟล์ข้อมูลการทดสอบของ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="212be-401">ตัวอย่างเช่น ป้อน หรือเลือก **C:\\Temp\\RegressionTool**</span><span class="sxs-lookup"><span data-stu-id="212be-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="212be-402">ถ้าชื่อของโฟลเดอร์มีช่องว่าง การดำเนินการจะล้มเหลวเนื่องจากไม่พบโฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="212be-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="212be-403">ปัญหานี้เป็นปัญหาที่ทราบ และควรได้รับการแก้ไขในเครื่องมือรุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="212be-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="212be-404">**เบราเซอร์เริ่มต้น** – เลือก **Internet Explorer** หรือ **Google Chrome** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="212be-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="212be-405">ตรวจสอบให้แน่ใจว่าได้ติดตั้งไดรเวอร์ของเบราว์เซอร์ที่เหมาะสมแล้ว</span><span class="sxs-lookup"><span data-stu-id="212be-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="212be-406">**การหมดเวลาของการรันการทดสอบ** – ระบุรอบระยะเวลาการหมดเวลาเป็นนาทีสำหรับการรันการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="212be-407">เมื่อรอบระยะเวลาของการหมดเวลาผ่านไป windows ที่ใช้งานอยู่ทั้งหมดจะถูกปิด และกรณีทดสอบที่ค้างอยู่จะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="212be-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="212be-408">**การหมดเวลาของการดำเนินการทดสอบ** – ฟิลด์นี้จะควบคุมรอบระยะเวลาการหมดเวลาเป็นนาที สำหรับการร้องขอเซิร์ฟเวอร์ของสภาพแวดล้อม Finance and Operation</span><span class="sxs-lookup"><span data-stu-id="212be-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="212be-409">โดยปกติแล้ว ค่าเริ่มต้น (2 นาที) ควรจะเพียงพอ</span><span class="sxs-lookup"><span data-stu-id="212be-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="212be-410">อย่างไรก็ตาม สำหรับสภาพแวดล้อมที่ช้าลง คุณอาจต้องการเพิ่มค่า ถ้าข้อผิดพลาดที่เกี่ยวข้องกับการหมดเวลาเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="212be-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="212be-411">**ชื่อบริษัท** – ป้อนชื่อบริษัทที่จะใช้เป็นบริษัท Finance and Operations เริ่มต้นของคุณ เมื่อมีการสร้างไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-411">**Company name** – Enter the company name to use as your default Finance and Operations company when Excel parameter files are created.</span></span> <span data-ttu-id="212be-412">คุณสามารถเปลี่ยนบริษัทได้ในภายหลัง โดยแก้ไขไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![กล่องโต้ตอบการตั้งค่า](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="212be-414">เลือก **นำไปใช้** เพื่อนำไปใช้และบันทึกการตั้งค่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="212be-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="212be-415">เมื่อต้องการบันทึกการตั้งค่าปัจจุบันของคุณลงในไฟล์การตั้งค่าคอนฟิกบนคอมพิวเตอร์ของคุณ ให้เลือก **บันทึกเป็น**</span><span class="sxs-lookup"><span data-stu-id="212be-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="212be-416">เมื่อต้องการคืนค่าการตั้งค่าของคุณจากไฟล์การตั้งค่าคอนฟิกบนคอมพิวเตอร์ของคุณ ให้เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="212be-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="212be-417">เลือก **ปิด** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="212be-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="212be-418">โหลดและรันกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-418">Load and run test cases</span></span>

1. <span data-ttu-id="212be-419">เลือก **โหลด** เพื่อโหลดแผนการทดสอบ **แผนการทดสอบ RSAT** จากโครงการ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![ปุ่มโหลด](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="212be-421">เลือกกรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่** จากชุดการทดสอบ แล้วเลือก **สร้าง \> สร้างไฟล์การดำเนินการทดสอบและไฟล์พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="212be-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![คำสั่งสร้างไฟล์การดำเนินการทดสอบและไฟล์พารามิเตอร์บนเมนูสร้าง](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="212be-423">ไฟล์พารามิเตอร์ของ Excel ถูกสร้างขึ้นในโฟลเดอร์เฉพาะที่ที่คุณระบุไว้ในการตั้งค่าคอนฟิก RSAT (ตัวอย่างเช่น **C:\\Temp\\RegressionTool**)</span><span class="sxs-lookup"><span data-stu-id="212be-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![ไฟล์พารามิเตอร์ Excel ถูกสร้างขึ้น](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="212be-425">ถ้าคุณต้องการบันทึกไฟล์พารามิเตอร์ ให้เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="212be-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="212be-426">ไฟล์การทดสอบระบบอัตโนมัติของกรณีการทดสอบที่เลือกทั้งหมดจะถูกอัปโหลดไปยัง Azure DevOps สำหรับการใช้งานในอนาคต</span><span class="sxs-lookup"><span data-stu-id="212be-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="212be-427">(ไฟล์เหล่านี้รวมถึงไฟล์พารามิเตอร์การทดสอบ Excel)</span><span class="sxs-lookup"><span data-stu-id="212be-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="212be-428">ด้วยวิธีนี้ คุณสามารถเลือก **โหลด** เพื่อโหลดไฟล์พารามิเตอร์ (และไฟล์ระบบอัตโนมัติ) จากกรณีการทดสอบโดยตรงจาก Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="212be-429">คุณไม่จำเป็นต้องสร้างไฟล์พารามิเตอร์ใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="212be-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="212be-430">วิธีการนี้จะกลายเป็นเรื่องสำคัญในภายหลัง เมื่อคุณต้องการรักษาการปรับเปลี่ยนในไฟล์พารามิเตอร์ และไม่ต้องการให้มีการเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="212be-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="212be-431">เมื่อต้องการตรวจสอบว่ามีการบันทึกไฟล์ระบบอัตโนมัติและไฟล์พารามิเตอร์ไปยัง Azure DevOps ไปที่โครงการ Azure DevOps เลือก **บอร์ด \> รายการงาน** และเลือกกรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="212be-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="212be-432">บนแท็บ **เอกสารแนบ** คุณควรเห็นไฟล์สี่ไฟล์:</span><span class="sxs-lookup"><span data-stu-id="212be-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="212be-433">ไฟล์ระบบอัตโนมัติ **.cs** – C\#</span><span class="sxs-lookup"><span data-stu-id="212be-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="212be-434">**.dll** – คอมไพล์ไฟล์ระบบอัตโนมัติเป็นแอสเซมบลี</span><span class="sxs-lookup"><span data-stu-id="212be-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="212be-435">**.xlsx** – ไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="212be-436">**.xml** – การบันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="212be-436">**.xml** – Recording file</span></span>

    ![ไฟล์บนแท็บเอกสารแนบ](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="212be-438">เลือกกรณีการทดสอบที่จะรัน แล้วเลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="212be-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-439">ก่อนที่คุณจะรันกรณีการทดสอบ ถ้าคุณกำลังใช้ Internet Explorer เป็นเบราว์เซอร์ ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่าความละเอียดเดสก์ทอปของคุณเป็น **100%** ที่ **การตั้งค่า Windows Display \> ขนาดและโครงร่าง**</span><span class="sxs-lookup"><span data-stu-id="212be-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="212be-440">หากคุณไม่สามารถเปลี่ยนการตั้งค่านี้บนเครื่องเสมือน (VM) ให้เปลี่ยนบนไคลเอนต์ (แล็ปท็อป) ที่คุณกำลังพยายามเข้าถึง VM</span><span class="sxs-lookup"><span data-stu-id="212be-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="212be-441">จากนั้น การตั้งค่าความละเอียดจะถูกสืบทอดมาจากการตั้งค่าการแสดงผล VM</span><span class="sxs-lookup"><span data-stu-id="212be-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![ความละเอียดเดสก์ท็อปที่ถูกตั้งค่าเป็น 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="212be-443">ถ้าไม่ได้ติดตั้งไดรเวอร์ของเบราว์เซอร์ไว้ในระบบ คุณจะได้รับข้อความแจ้งเตือนที่ระบุว่า "การดำเนินการนี้จำเป็นต้องมีไดรเวอร์ \<ชื่อเบราว์เซอร์\></span><span class="sxs-lookup"><span data-stu-id="212be-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="212be-444">คุณต้องการดาวน์โหลดและติดตั้งเดี๋ยวนี้โดยอัตโนมัติหรือไม่?"</span><span class="sxs-lookup"><span data-stu-id="212be-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="212be-445">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="212be-445">Select **Yes**.</span></span>

    ![ข้อความเตือนสำหรับ Internet Explorer](./media/setup_rsa_tool_69.png)

    ![ข้อความเตือนสำหรับ Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="212be-448">หากคุณใช้ Chrome เป็นเบราว์เซอร์ และได้รับข้อความแสดงข้อผิดพลาดที่แจ้งว่ารอบเวลาไม่ถูกสร้างได้เนื่องจากรุ่นของ Chrome ไม่ถูกต้อง ให้ดาวน์โหลดไดรเวอร์ Chrome ล่าสุดจาก <http://chromedriver.chromium.org/downloads> ไปยังโฟลเดอร์ **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**</span><span class="sxs-lookup"><span data-stu-id="212be-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![ข้อความแสดงข้อผิดพลาดสำหรับ Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="212be-450">มีการรันกรณีการทดสอบ และมีการปรับปรุงฟิลด์ **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="212be-450">The test case is run, and the **Result** field is updated.</span></span>

    ![ตัวบ่งชี้ความก้าวหน้า](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="212be-452">ถ้าคุณได้ทำตามบทช่วยสอนนี้ตามที่มีการเขียน กรณีการทดสอบ **สร้างผลิตภัณฑ์ใหม่** จะล้มเหลว เนื่องจากการบันทึกงานสำหรับการสร้างผลิตภัณฑ์ที่บันทึกชื่อผลิตภัณฑ์เป็นค่าที่มีรหัสแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="212be-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="212be-453">ถ้าคุณรันกรณีทดสอบเดียวกันอีกครั้ง คุณควรได้รับข้อความแสดงข้อผิดพลาด เนื่องจากมีผลิตภัณฑ์อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="212be-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![ฟิลด์ผลลัพธ์ที่ถูกตั้งค่าเป็น ล้มเหลว](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="212be-455">ดูผลลัพธ์ของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-455">View the test results</span></span>

1. <span data-ttu-id="212be-456">คลิกสองครั้งที่กรณีการทดสอบที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="212be-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="212be-457">คุณได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="212be-457">You receive an error message.</span></span>

    ![ข้อความแสดงข้อผิดพลาด](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="212be-459">เลือก **รายละเอียด** เพื่อดูข้อความแสดงข้อผิดพลาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="212be-459">Select **Details** to view the whole error message.</span></span>

    ![ข้อความแสดงข้อผิดพลาดทั้งหมด](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="212be-461">เมื่อต้องการดูรุ่นโดยละเอียดของข้อความแสดงข้อผิดพลาดใน Azure DevOps เลือก **เปิดใน Azure DevOps**</span><span class="sxs-lookup"><span data-stu-id="212be-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="212be-462">ใน Azure DevOps คุณสามารถดูสถานะของกรณีการทดสอบและข้อความแสดงข้อผิดพลาดโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="212be-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![ข้อความแสดงข้อผิดพลาดโดยละเอียดใน Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="212be-464">เมื่อต้องการดูผลการทดสอบโดยตรงในโครงการ Azure DevOps ให้ไปที่ **แผนการทดสอบ \> แผนการทดสอบ \> การรัน**</span><span class="sxs-lookup"><span data-stu-id="212be-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="212be-465">คลิกสองครั้งที่การรันการทดสอบที่คุณต้องการดูรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="212be-465">Double-click the test run that you want to see more details for.</span></span>

    ![รายการของการรันการทดสอบใน Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="212be-467">แท็บ **รันสรุป** จะบ่งชี้ว่ากรณีการทดสอบล้มเหลว แต่ไม่ได้ระบุข้อความแสดงข้อผิดพลาดจริง</span><span class="sxs-lookup"><span data-stu-id="212be-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="212be-468">เมื่อต้องการดูข้อความแสดงข้อผิดพลาดโดยละเอียด ให้เลือกแท็บ **ผลการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="212be-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![แท็บรันสรุป](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="212be-470">แท็บ **ผลการทดสอบ** จะให้ข้อมูลกรณีการทดสอบ พร้อมกับผลลัพธ์และข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="212be-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![แท็บผลการทดสอบ](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="212be-472">คลิกสองครั้งที่เรกคอร์ดที่เกี่ยวข้องเพื่อดูข้อความแสดงข้อผิดพลาดโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="212be-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![ข้อความแสดงข้อผิดพลาดโดยละเอียด](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="212be-474">นอกจากนี้ ข้อความแสดงข้อผิดพลาดทั้งหมดยังพร้อมใช้งานเฉพาะที่ใน **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**</span><span class="sxs-lookup"><span data-stu-id="212be-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="212be-475">นอกจากนี้ คุณยังสามารถส่งออกผลการรันการทดสอบจากระดับแผนทดสอบได้ ด้วยการเลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="212be-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![การส่งออกแผนการทดสอบ](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="212be-477">ปรับเปลี่ยนไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="212be-478">เปิด RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-478">Open RSAT.</span></span>
2. <span data-ttu-id="212be-479">เลือกกล่องการทดสอบ แล้วจากนั้น เลือก **แก้ไข** เพื่อเปิดไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="212be-480">บนแผ่นงาน **EcoResProductCreate** โปรดทราบว่าค่าของฟิลด์ **หมายเลขผลิตภัณฑ์** มีรหัสแบบตายตัว</span><span class="sxs-lookup"><span data-stu-id="212be-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="212be-481">คุณต้องปรับปรุงฟิลด์นี้เป็นหมายเลขผลิตภัณฑ์ใหม่ ก่อนที่คุณจะรันกรณีการทดสอบอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="212be-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="212be-482">เมื่อต้องการสร้างหมายเลขผลิตภัณฑ์ที่ไม่ซ้ำกันสำหรับการรันแต่ละครั้งโดยไม่ต้องเปิดไฟล์พารามิเตอร์ Excel อีกครั้ง และปรับปรุงหมายเลขผลิตภัณฑ์ด้วยตนเองทุกครั้ง ใช้สูตรของ Excel ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="212be-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="212be-483">นอกจากแท็บ **ทั่วไป** ไฟล์พารามิเตอร์ของ Excel จะมีแท็บข้อมูลสำหรับหน้าแบบฟอร์ม Finance and Operations ทั้งหมดที่กรณีการทดสอบเยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="212be-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every Finance and Operations form page the test case visits.</span></span>

    ![ฟิลด์หมายเลขผลิตภัณฑ์](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="212be-485">เลือก **บันทึก** และจากนั้น ปิดสมุดงาน Excel</span><span class="sxs-lookup"><span data-stu-id="212be-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="212be-486">เลือก **อัปโหลด** เพื่อบันทึกไฟล์พารามิเตอร์ของ Excel ไปยัง Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![ข้อความการอัปโหลดสำเร็จ](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="212be-488">เมื่อต้องการรันกรณีการทดสอบในบริบทของผู้ใช้ที่ระบุ ให้ป้อนรหัสอีเมลของผู้ใช้ในฟิลด์ **ผู้ใช้การทดสอบ** บนแท็บ **ทั่วไป** ของไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="212be-489">ในรุ่นล่าสุดของ RSAT จะมีการปรับปรุงโครงร่างของฟิลด์ในไฟล์พารามิเตอร์ของ Excel แต่แนวคิดยังคงอยู่เหมือนเดิม</span><span class="sxs-lookup"><span data-stu-id="212be-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![ฟิลด์ผู้ใช้การทดสอบ](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="212be-491">ตรวจสอบความถูกต้องของผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="212be-491">Validate the results</span></span>

- <span data-ttu-id="212be-492">เลือก **รัน** เพื่อรันกรณีการทดสอบอีกครั้ง และตรวจสอบว่ากรณีการทดสอบผ่าน</span><span class="sxs-lookup"><span data-stu-id="212be-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="212be-493">คุณสามารถดูผลการทดสอบตามที่อธิบายไว้ในส่วน [ดูผลการทดสอบ](#view-the-test-results)</span><span class="sxs-lookup"><span data-stu-id="212be-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![ฟิลด์ผลลัพธ์ที่ถูกตั้งค่าเป็น ผ่าน](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="212be-495">กลุ่มของกรณีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="212be-495">Chaining of test cases</span></span>

<span data-ttu-id="212be-496">คุณลักษณะที่สำคัญอย่างหนึ่งของ RSAT คือการเชื่อมโยงของกรณีการทดสอบ (นั่นคือ ความสามารถของการทดสอบเพื่อส่งผ่านค่าไปยังการทดสอบอื่นๆ)</span><span class="sxs-lookup"><span data-stu-id="212be-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="212be-497">กรณีการทดสอบจะรันตามลำดับที่กำหนดในแผนการทดสอบ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="212be-498">(ลำดับนี้ยังสามารถถูกปรับปรุงได้ในเครื่องมือการทดสอบเอง) ดังนั้น ถ้าคุณต้องการส่งผ่านตัวแปรจากกรณีการทดสอบหนึ่งไปยังอีกกรณีหนึ่ง อาจเป็นเรื่องสำคัญมากที่การทดสอบจะต้องอยู่ในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="212be-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="212be-499">ในส่วนนี้ คุณจะสร้างตัวแปรที่บันทึกไว้ในกรณีการทดสอบครั้งแรก สร้างกรณีการทดสอบที่สอง และส่งผ่านตัวแปรที่บันทึกไว้จากกรณีการทดสอบครั้งแรกไปยังกรณีการทดสอบครั้งที่สอง</span><span class="sxs-lookup"><span data-stu-id="212be-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="212be-500">จากนั้น คุณจะสามารถรันกรณีการทดสอบเป็นกรณีการทดสอบที่เชื่อมโยงได้ใน RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="212be-501">แก้ไขการบันทึกงานที่มีอยู่ เมื่อต้องการสร้างตัวแปรที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="212be-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="212be-502">เปิดไคลเอนต์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="212be-502">Open the Finance and Operations client.</span></span>
2. <span data-ttu-id="212be-503">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) แล้วจากนั้น เลือก **ตัวบันทึกงาน**</span><span class="sxs-lookup"><span data-stu-id="212be-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="212be-504">เลือก **แก้ไขการบันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-504">Select **Edit Recording**.</span></span>

    ![ปุ่มแก้ไขการบันทึก](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="212be-506">เลือก **เปิดจาก Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="212be-506">Select **Open from Lifecycle Services**.</span></span>

    ![ปุ่มเปิดจาก Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="212be-508">เลือก **เลือกไลบรารี Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="212be-508">Select **Select the Lifecycle Services library**.</span></span>

    ![เลือกปุ่มไลบรารี Lifecycle Services](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="212be-510">ไลบรารี BPM ถูกโหลดจาก LCS</span><span class="sxs-lookup"><span data-stu-id="212be-510">BPM libraries are loaded from LCS.</span></span>

    ![ตัวบ่งชี้ความก้าวหน้า](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="212be-512">หลังจากที่มีการโหลดไลบรารี BPM จาก LCS ให้เลือกไลบรารี BPM ของ **RSAT** และกระบวนการทางธุรกิจ **สร้างผลิตภัณฑ์ใหม่** ที่มีการเชื่อมโยงกับการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="212be-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="212be-513">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="212be-513">Then select **OK**.</span></span>

    ![การเลือกไลบรารี BPM และกระบวนการทางธุรกิจ](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="212be-515">ชื่อของการบันทึกงานที่เหมาะสมถูกป้อนในฟิลด์ **ชื่อของการบันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="212be-516">เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="212be-516">Select **Start**.</span></span>

    ![ชื่อของการบันทึกงานในฟิลด์ชื่อของการบันทึก](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="212be-518">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์** และเลือก **สร้าง** เพื่อเปิดหน้าที่การบันทึกงานดั้งเดิม **สร้างผลิตภัณฑ์** ถูกบันทึก</span><span class="sxs-lookup"><span data-stu-id="212be-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="212be-519">เลือก **ขั้นตอนการแทรก**</span><span class="sxs-lookup"><span data-stu-id="212be-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-520">จะมีการแทรกขั้นตอนใหม่ **หลังจาก** ขั้นตอนที่คุณเลือกไว้ในบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="212be-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![ปุ่มแทรกขั้นตอน](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="212be-522">คลิกขวาที่ฟิลด์ **หมายเลขผลิตภัณฑ์** แล้วเลือก **ตัวบันทึกงาน \> คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="212be-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![คัดลอกคำสั่ง](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="212be-524">มีการเพิ่มขั้นตอนใหม่ในบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="212be-524">A new step is added in the pane.</span></span> <span data-ttu-id="212be-525">จัดทำบันทึกของค่าในฟิลด์ **หมายเลขผลิตภัณฑ์** เนื่องจากคุณจะต้องใช้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="212be-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![เพิ่มขั้นตอนใหม่แล้ว](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="212be-527">เลือก **ทำการแก้ไขเสร็จสิ้นแล้ว**</span><span class="sxs-lookup"><span data-stu-id="212be-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="212be-528">เลือก **บันทึกไปยัง Lifecycle Services** และเชื่อมโยงการบันทึกงานใหม่กับไลบรารี BPM เดียวกัน และกระบวนการทางธุรกิจที่เกี่ยวข้องกับการบันทึกงานดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="212be-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="212be-529">สำหรับข้อมูลเพิ่มเติม ดูส่วน [สร้างการบันทึกงาน และบันทึกไปยังไลบรารี BPM](#create-a-task-recording-and-save-it-to-the-bpm-library)</span><span class="sxs-lookup"><span data-stu-id="212be-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="212be-530">ไปยังไลบรารี BPM และเลือก **ซิงค์กรณีการทดสอบ** เพื่อเขียนทับการบันทึกงานที่แนบอยู่กับกรณีการทดสอบใน Azure DevOps ตามที่อธิบายไว้ในส่วน [ทดสอบการซิงโครไนส์จาก BPM ไปยัง Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)</span><span class="sxs-lookup"><span data-stu-id="212be-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="212be-531">เปิด RSAT และเลือก **โหลด** เพื่อโหลดกรณีการทดสอบทั้งหมดในชุดทดสอบอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="212be-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="212be-532">คุณต้องสร้างไฟล์ระบบอัตโนมัติและไฟล์พารามิเตอร์อีกครั้งสำหรับกรณีการทดสอบที่เหมาะสม โดยเลือกกรณีการทดสอบ และจากนั้น เลือก **สร้าง \> สร้างไฟล์การดำเนินการและและไฟล์พารามิเตอร์** ตามที่อธิบายไว้ในส่วน [โหลดและรันกรณีการทดสอบ](#load-and-run-test-cases)</span><span class="sxs-lookup"><span data-stu-id="212be-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-533">ถ้าไฟล์พารามิเตอร์ Excel ถูกเปิดค้างไว้ การสร้างใหม่จะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="212be-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="212be-534">ดังนั้น โปรดตรวจสอบให้แน่ใจว่ามีการปิดไฟล์พารามิเตอร์ Excel สำหรับกรณีการทดสอบ ก่อนที่คุณจะสร้างไฟล์พารามิเตอร์ Excel ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="212be-535">เลือก **แก้ไข** เพื่อเปิดไฟล์พารามิเตอร์ Excel ใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="212be-536">คุณจะเห็นรายการ **ตัวแปรที่บันทึกไว้** ใหม่บนบรรทัดที่ 9</span><span class="sxs-lookup"><span data-stu-id="212be-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="212be-537">ตัวแปรนี้ **{{EcoResProductCreate\_รหัสประจำตัว\_ProductNumber\_คัดลอก}}** ถูกบันทึกไว้ในไฟล์ XML ของการบันทึกงาน และสามารถใช้ในการทดสอบในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="212be-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![รายการตัวแปรที่บันทึกไว้](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="212be-539">สร้างกรณีการทดสอบใหม่</span><span class="sxs-lookup"><span data-stu-id="212be-539">Create a new test case</span></span>

1. <span data-ttu-id="212be-540">ไปที่ไลบรารี BPM ของ **RSAT**</span><span class="sxs-lookup"><span data-stu-id="212be-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="212be-541">เลือกกระบวนการ **กระบวนการทางธุรกิจที่สนับสนุนของตัวอย่าง** และจากนั้น ทางด้านขวา ให้เลือก **โหมดแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="212be-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="212be-542">เปลี่ยนค่าของทั้งฟิลด์ **ชื่อ** และฟิลด์ **คำอธิบาย** เพื่อ **นำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="212be-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="212be-543">จากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="212be-543">Then select **Save**.</span></span>

    ![ชื่อและคำอธิบายที่เปลี่ยนไปเพื่อนำผลิตภัณฑ์ออกใช้](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="212be-545">สร้างการบันทึกงานใหม่ที่มีฟังก์ชันการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="212be-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="212be-546">สร้างการบันทึกงานเพื่อนำผลิตภัณฑ์ที่สร้างไว้ก่อนหน้านี้ออกใช้ไปยังนิติบุคคล USRT</span><span class="sxs-lookup"><span data-stu-id="212be-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="212be-547">สำหรับข้อมูลเพิ่มเติม ดูส่วน [สร้างการบันทึกงาน และบันทึกไปยังไลบรารี BPM](#create-a-task-recording-and-save-it-to-the-bpm-library)</span><span class="sxs-lookup"><span data-stu-id="212be-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="212be-548">สำหรับกรณีการทดสอบที่เชื่อมโยง เราขอแนะนำให้คุณค้นหาหรือกรองข้อมูลสำหรับเรกคอร์ดที่คุณต้องการด้วย *การพิมพ์ค่าของฟิลด์ด้วยตนเอง*</span><span class="sxs-lookup"><span data-stu-id="212be-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="212be-549">ในลักษณะนี้ เครื่องมือนี้จะสามารถกำหนดว่าจะมีการดำเนินการกับเรกคอร์ดที่ต้องใช้ในกรณีการทดสอบในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="212be-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![การบันทึกงานใหม่ที่มีฟังก์ชันการตรวจสอบความถูกต้อง](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="212be-551">เมื่อภาพประกอบก่อนหน้านี้แสดงขึ้น หลังจากที่พบผลิตภัณฑ์โดยใช้ตัวกรองด่วน แต่ก่อนที่คุณจะเลือก **นำผลิตภัณฑ์ออกใช้** คุณจะตรวจสอบความถูกต้องของค่าของฟิลด์ **หมายเลขผลิตภัณฑ์** เพื่อให้แน่ใจว่ารหัสผลิตภัณฑ์เป็นรหัสผลิตภัณฑ์ที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="212be-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="212be-552">เมื่อต้องการตรวจสอบความถูกต้องของค่า คลิกขวาที่ฟิลด์ **หมายเลขผลิตภัณฑ์** และจากนั้น เลือก **ตัวบันทึกงาน \> ตรวจสอบความถูกต้อง \> ค่าปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="212be-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![การตรวจสอบความถูกต้องของค่าปัจจุบัน](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="212be-554">บันทึกการบันทึกงานไปยัง BPM</span><span class="sxs-lookup"><span data-stu-id="212be-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="212be-555">หลังจากเสร็จสิ้นการบันทึกงาน เลือก **บันทึกไปยัง Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="212be-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![ตัวเลือกบันทึก](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="212be-557">ข้อมูลไลบรารีถูกโหลดจาก LCS</span><span class="sxs-lookup"><span data-stu-id="212be-557">Library information is loaded from LCS.</span></span>

    ![ตัวบ่งชี้ความก้าวหน้า](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="212be-559">เลือกไลบรารี BPM เพื่อเชื่อมโยงกับการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="212be-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="212be-560">สำหรับบทช่วยสอนนี้ ให้เลือกไลบรารี BPM ของ **RSAT** ที่สร้างไว้ก่อนหน้านี้ และ **นำผลิตภัณฑ์ออกใช้** ที่กระบวนการทางธุรกิจอยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="212be-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="212be-561">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="212be-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="212be-562">ซิงค์ BPM กับ Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="212be-563">ไปยังไลบรารี BPM และเปิดไลบรารี **RSAT**</span><span class="sxs-lookup"><span data-stu-id="212be-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="212be-564">เลือก **ซิงค์ VSTS** แล้วจากนั้น **ซิงค์กรณีการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="212be-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="212be-565">สำหรับข้อมูลเพิ่มเติม ดูส่วน [ทดสอบการซิงโครไนส์จาก BPM ไปยัง Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)</span><span class="sxs-lookup"><span data-stu-id="212be-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="212be-566">หลังจากการซิงโครไนส์เสร็จสมบูรณ์แล้ว รายการงานใหม่และกรณีการทดสอบที่เกี่ยวข้องสำหรับกระบวนการทางธุรกิจ **นำผลิตภัณฑ์ออกใช้** ใน Azure DevOps ที่ **บอร์ด \> รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="212be-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="212be-567">เพิ่มกรณีการทดสอบใหม่ไปยังชุดการทดสอบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="212be-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="212be-568">ไปที่ **แผนการทดสอบ \> แผนการทดสอบ** และเลือกแผน **แผนการทดสอบ RSAT**</span><span class="sxs-lookup"><span data-stu-id="212be-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="212be-569">เลือก **เพิ่มรายการที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="212be-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="212be-570">ในหน้า **เพิ่มกรณีการทดสอบไปยังชุด** ให้เลือก **รันการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="212be-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="212be-571">เลือกกรณีการทดสอบใหม่ที่สร้างขึ้นสำหรับ **นำผลิตภัณฑ์ออกใช้** แล้วจากนั้น เลือก **เพิ่มกรณีการทดสอบ** ที่มุมล่างด้านล่างขวาของหน้า (ปุ่มนี้จะไม่แสดงในภาพประกอบต่อไปนี้)</span><span class="sxs-lookup"><span data-stu-id="212be-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![หน้าเพิ่มกรณีการทดสอบไปยังชุด](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="212be-573">ตอนนี้ชุดการทดสอบมีกรณีการทดสอบสองกรณี</span><span class="sxs-lookup"><span data-stu-id="212be-573">The test suite now has two test cases.</span></span>

    ![กรณีการทดสอบสองกรณีในชุดการทดสอบ](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="212be-575">โหลดกรณีการทดสอบลงใน RSAT</span><span class="sxs-lookup"><span data-stu-id="212be-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="212be-576">เปิด RSAT แล้วเลือก **โหลด**</span><span class="sxs-lookup"><span data-stu-id="212be-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="212be-577">มีการโหลดกรณีการทดสอบ และคุณได้รับคำเตือนที่ระบุว่า "การดำเนินการนี้จะเขียนทับไฟล์ข้อมูลการทดสอบของ Excel การเปลี่ยนแปลงเฉพาะที่จะสูญหายไป</span><span class="sxs-lookup"><span data-stu-id="212be-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="212be-578">คุณต้องการดำเนินการต่อหรือไม่?"</span><span class="sxs-lookup"><span data-stu-id="212be-578">Do you want to proceed?"</span></span> <span data-ttu-id="212be-579">เลือก **ใช่** เพื่อปรับปรุงไฟล์พารามิเตอร์ Excel ในระบบเฉพาะที่ แต่ไม่ใช่ไฟล์พารามิเตอร์ excel ที่ถูกอัปโหลดไปยัง Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![ข้อความเตือน](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="212be-581">มีการโหลดกรณีการทดสอบทั้งสองกรณี พร้อมกับไฟล์พารามิเตอร์ Excel สำหรับกรณีการทดสอบแรก</span><span class="sxs-lookup"><span data-stu-id="212be-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="212be-582">เนื่องจากคุณเลือก **อัปโหลด** ในการรันครั้งล่าสุด ไฟล์พารามิเตอร์จะถูกดึงมาจาก Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="212be-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![โหลดกรณีการทดสอบแล้ว](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="212be-584">เลือกเฉพาะกรณีการทดสอบที่สอง แล้วจากนั้น เลือก **สร้าง \> สร้างการดำเนินการทดสอบและไฟล์พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="212be-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="212be-585">แก้ไขไฟล์พารามิเตอร์ของ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="212be-586">เลือกเฉพาะกรณีการทดสอบที่สอง แล้วจากนั้น เลือก **แก้ไข** เพื่อเปิดไฟล์พารามิเตอร์ Excel ที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="212be-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="212be-587">คัดลอกตัวแปรที่บันทึกไว้ **{{EcoResProductCreate\_รหัสประจำตัว\_ProductNumber\_คัดลอก}}** (ดูส่วน [ปรับเปลี่ยนการบันทึกงานที่มียู่เพื่อสร้างตัวแปรที่บันทึกไว้](#modify-an-existing-task-recording-to-create-a-saved-variable) ) จากกรณีการทดสอบแรก ลงในฟิลด์ทั้งหมดที่มีการใช้หมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="212be-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="212be-588">ในกรณีนี้ คุณคัดลอกตัวแปรไปยังฟิลด์ **หมายเลขผลิตภัณฑ์** และฟิลด์ **ตรวจสอบความถูกต้องของหมายเลขผลิตภัณฑ์** บนแผ่นงาน **EcoResProductListPage**</span><span class="sxs-lookup"><span data-stu-id="212be-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![ฟิลด์หมายเลขผลิตภัณฑ์และฟิลด์ตรวจสอบความถูกต้องของหมายเลขผลิตภัณฑ์](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="212be-590">สามารถส่งผ่านตัวแปรระหว่างการทดสอบได้เฉพาะในระหว่างการรันการทดสอบเดียวกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="212be-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="212be-591">ชื่อของตัวแปรต้องตรงกัน</span><span class="sxs-lookup"><span data-stu-id="212be-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="212be-592">เลือก **บันทึก** และจากนั้น ปิดสมุดงาน Excel</span><span class="sxs-lookup"><span data-stu-id="212be-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="212be-593">เลือก **อัปโหลด** เพื่อบันทึกการเปลี่ยนแปลงที่คุณทำไว้กับไฟล์พารามิเตอร์ Excel</span><span class="sxs-lookup"><span data-stu-id="212be-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="212be-594">รันกรณีทดสอบที่ถูกเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="212be-594">Run the chained test cases</span></span>

1. <span data-ttu-id="212be-595">เลือกกรณีการทดสอบทั้งสองกรณี แล้วเลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="212be-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="212be-596">ตรวจสอบว่ากรณีการทดสอบทั้งสองกรณีผ่าน</span><span class="sxs-lookup"><span data-stu-id="212be-596">Verify that both test cases have passed.</span></span>

    ![ฟิลด์ผลลัพธ์ที่ถูกตั้งค่าเป็น ผ่าน สำหรับกรณีการทดสอบทั้งสองกรณี](./media/setup_rsa_tool_105.png)
