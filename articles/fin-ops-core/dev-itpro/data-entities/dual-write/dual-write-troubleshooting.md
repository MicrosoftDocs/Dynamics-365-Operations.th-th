---
title: การแก้ไขปัญหาเบื้องต้นทั่วไป
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาเบื้องต้นทั่วไปสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 6356ec6850667f32f9e9e4133686c40f0b6d76d7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688270"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="9b29f-103">การแก้ไขปัญหาเบื้องต้นทั่วไป</span><span class="sxs-lookup"><span data-stu-id="9b29f-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="9b29f-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาเบื้องต้นทั่วไปสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="9b29f-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b29f-105">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="9b29f-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="9b29f-106">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9b29f-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="9b29f-107">เมื่อคุณพยายามติดตั้งแพคเกจการรวมแบบสองทิศทางโดยใช้เครื่องมือ Package Deployer ไม่มีโซลูชันที่พร้อมใช้งานแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="9b29f-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="9b29f-108">เครื่องมือ Package Deployer บางรุ่นเข้ากันไม่ได้กับแพคเกจโซลูชันการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="9b29f-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="9b29f-109">เมื่อติดตั้งแพคเกจเสร็จเรียบร้อยแล้ว ให้ตรวจสอบให้แน่ใจว่าได้ใช้ [รุ่น 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) หรือรุ่นที่ใหม่กว่าของเครื่องมือ Package Deployer</span><span class="sxs-lookup"><span data-stu-id="9b29f-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="9b29f-110">หลังจากที่คุณติดตั้งเครื่องมือ Package Deployer แล้ว ให้ติดตั้งแพคเกจโซลูชันโดยทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9b29f-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="9b29f-111">ดาวน์โหลดไฟล์แพคเกจโซลูชันล่าสุดจาก Yammer.com</span><span class="sxs-lookup"><span data-stu-id="9b29f-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="9b29f-112">หลังจากดาวน์โหลดไฟล์ zip ของแพคเกจแล้ว ให้คลิกขวา และเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="9b29f-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="9b29f-113">เลือกกล่องกาเครื่องหมาย **ยกเลิกการบล็อค** และจากนั้น เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="9b29f-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="9b29f-114">ถ้าคุณไม่เห็นกล่องกาเครื่องหมาย **ยกเลิกการบล็อค** ไฟล์ zip ถูกยกเลิกการบล็อคเรียบร้อยแล้ว และคุณสามารถข้ามขั้นตอนนี้ได้</span><span class="sxs-lookup"><span data-stu-id="9b29f-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![กล่องโต้ตอบคุณสมบัติ](media/unblock_option.png)

2. <span data-ttu-id="9b29f-116">แยกไฟล์ zip ของแพคเกจ และคัดลอกไฟล์ทั้งหมดในโฟลเดอร์ **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**</span><span class="sxs-lookup"><span data-stu-id="9b29f-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![เนื้อหาของโฟลเดอร์ Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="9b29f-118">วางไฟล์ที่คัดลอกทั้งหมดไปยังโฟลเดอร์ **เครื่องมือ** ของเครื่องมือ Package Deployer</span><span class="sxs-lookup"><span data-stu-id="9b29f-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="9b29f-119">รัน **PackageDeployer.exe** เพื่อเลือกสภาพแวดล้อม Dataverse และติดตั้งโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="9b29f-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![เนื้อหาของโฟลเดอร์เครื่องมือ](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="9b29f-121">เปิดใช้งานและดูล็อกการติดตามปลั๊กอินใน Dataverse เพื่อดูรายละเอียดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9b29f-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="9b29f-122">**บทบาทที่จำเป็นในการเปิดล็อกการติดตามและดูข้อผิดพลาด:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9b29f-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="9b29f-123">หากต้องการเปิดล็อกการติดตาม ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9b29f-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="9b29f-124">ลงชื่อเข้าใช้แอปที่เป็นแบบโมเดลใน Dynamics 365 เปิดหน้า **การตั้งค่า** และจากนั้น ภายใต้ **ระบบ** ให้เลือก **การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="9b29f-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="9b29f-125">บนหน้า **การจัดการ** เลือก **การตั้งค่าระบบ**</span><span class="sxs-lookup"><span data-stu-id="9b29f-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="9b29f-126">บนแท็บ **การกำหนดค่า** ในฟิลด์ **ปลั๊กอินและการสืบค้นกลับกิจกรรมลำดับงานที่กำหนดเอง** เลือก **ทั้งหมด** เพื่อเปิดใช้งานล็อกการติดตามปลั๊กอิน</span><span class="sxs-lookup"><span data-stu-id="9b29f-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="9b29f-127">ถ้าคุณต้องการบันทึกล็อกการติดตามเฉพาะเมื่อมีข้อยกเว้นเกิดขึ้น คุณสามารถเลือก **ข้อยกเว้น** แทนได้</span><span class="sxs-lookup"><span data-stu-id="9b29f-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="9b29f-128">หากต้องการดูการติดตาม ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9b29f-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="9b29f-129">ลงชื่อเข้าใช้แอปที่เป็นแบบโมเดลใน Dynamics 365 เปิดหน้า **การตั้งค่า** และจากนั้น ภายใต้ **การกำหนดเอง** ให้เลือก **ล็อกการติดตามปลั๊กอิน**</span><span class="sxs-lookup"><span data-stu-id="9b29f-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="9b29f-130">ค้นหาล็อกการติดตามที่ซึ่งฟิลด์ **ชื่อชนิด** ถูกตั้งค่าเป็น **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**</span><span class="sxs-lookup"><span data-stu-id="9b29f-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="9b29f-131">ดับเบิลคลิกที่รายการเพื่อดูล็อกทั้งหมด และจากนั้น บน FastTab **การดำเนินการ** ให้ตรวจสอบข้อความ **บล็อคข้อความ**</span><span class="sxs-lookup"><span data-stu-id="9b29f-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="9b29f-132">เปิดใช้งานโหมดดีบักเมื่อต้องการแก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริงในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="9b29f-133">**บทบาทที่จำเป็นในการดูข้อผิดพลาด:** ข้อผิดพลาดในการรวมแบบสองทิศทางของผู้ดูแลระบบซึ่งเกิดขึ้นใน Dataverse สามารถปรากฏขึ้นในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="9b29f-134">ในบางกรณี ข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดจะไม่พร้อมใช้งาน เนื่องจากข้อความยาวเกินไปหรือมีข้อมูลการระบุถึงตัวบุคคล (PII)</span><span class="sxs-lookup"><span data-stu-id="9b29f-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="9b29f-135">คุณสามารถเปิดใช้งานการบันทึกก verbose สำหรับข้อผิดพลาดได้โดยปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9b29f-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="9b29f-136">การตั้งค่าคอนฟิกโครงการทั้งหมดในแอป Finance and Operations มีคุณสมบัติ **IsDebugMode** ในเอนทิตี้ **DualWriteProjectConfiguration**</span><span class="sxs-lookup"><span data-stu-id="9b29f-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="9b29f-137">เปิดเอนทิตี้ **DualWriteProjectConfiguration** โดยใช้ add-in ของ Excel</span><span class="sxs-lookup"><span data-stu-id="9b29f-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="9b29f-138">วิธีง่ายๆ ในการเปิดเอนทิตี้คือ การเปิดใช้งานโหมด **การออกแบบ** ใน add-in ของ Excel และจากนั้น เพิ่ม **DualWriteProjectConfigurationEntity** ไปยังแผ่นงาน</span><span class="sxs-lookup"><span data-stu-id="9b29f-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="9b29f-139">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดข้อมูลเอนทิตี้ใน Excel และปรับปรุงโดยใช้ add-in ของ Excel](../../office-integration/use-excel-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="9b29f-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="9b29f-140">ตั้งค่าคุณสมบัติ **IsDebugMode** เป็น **ใช่** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="9b29f-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="9b29f-141">รันสถานการณ์จำลองที่กำลังสร้างข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9b29f-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="9b29f-142">ล็อก verbose พร้อมใช้งานในตาราง DualWriteErrorLog</span><span class="sxs-lookup"><span data-stu-id="9b29f-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="9b29f-143">เมื่อต้องการค้นหาข้อมูลในเบราว์เซอร์ตาราง ให้ใช้ URL ต่อไปนี้ (แทนที่ **XXX** ตามความเหมาะสม):</span><span class="sxs-lookup"><span data-stu-id="9b29f-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="9b29f-144">ตรวจสอบข้อผิดพลาดของการซิงโครไนส์บนเครื่องเสมือนสำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="9b29f-145">**บทบาทที่จำเป็นในการดูข้อผิดพลาด:** ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9b29f-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="9b29f-146">ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9b29f-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="9b29f-147">เปิดโครงการ LCS ที่คุณเลือกเพื่อทำการทดสอบการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="9b29f-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="9b29f-148">เลือกไทล์ **สภาพแวดล้อมที่โฮสต์ระบบคลาวด์**</span><span class="sxs-lookup"><span data-stu-id="9b29f-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="9b29f-149">ใช้ Remote Desktop เพื่อลงชื่อเข้าใช้ในเครื่องเสมือน (VM) สำหรับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="9b29f-150">ใช้บัญชีเฉพาะที่ที่แสดงอยู่ใน LCS</span><span class="sxs-lookup"><span data-stu-id="9b29f-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="9b29f-151">เปิดตัวแสดงเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="9b29f-151">Open Event viewer.</span></span>
6. <span data-ttu-id="9b29f-152">เลือก **ล็อกของแอพลิเคชันและบริการ \> Microsoft \> Dynamics \> AX-DualWriteSync \> การดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="9b29f-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="9b29f-153">ตรวจทานรายการของข้อผิดพลาดล่าสุด</span><span class="sxs-lookup"><span data-stu-id="9b29f-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="9b29f-154">ยกเลิกการเชื่อมโยงและเชื่อมโยงสภาพแวดล้อม Dataverse อื่นจากแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="9b29f-155">**บทบาทที่จำเป็นในการยกเลิกการเชื่อมโยงสภาพแวดล้อม:** ผู้ดูแลระบบสำหรับแอป Finance and Operations หรือ Dataverse</span><span class="sxs-lookup"><span data-stu-id="9b29f-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="9b29f-156">ลงชื่อเข้าใช้แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="9b29f-157">ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือกไทล์ **การรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="9b29f-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="9b29f-158">เลือกการแม็ปที่กำลังรันทั้งหมด และจากนั้น เลือก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="9b29f-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="9b29f-159">เลือก **ยกเลิกการเชื่อมโยงสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="9b29f-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="9b29f-160">เลือก **ใช่** เพื่อยืนยันการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="9b29f-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="9b29f-161">ขณะนี้คุณสามารถเชื่อมโยงสภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="9b29f-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="9b29f-162">ไม่สามารถดูฟอร์มข้อมูลรายการใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="9b29f-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="9b29f-163">เมื่อคุณสร้างใบสั่งขายใน Dynamics 365 Sales การคลิก **+เพิ่มผลิตภัณฑ์** อาจเปลี่ยนเส้นทางคุณไปยังฟอร์มรายการใบสั่งการดำเนินงานของโครงการ Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="9b29f-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="9b29f-164">ไม่มีวิธีการจากฟอร์มนั้นในการดูฟอร์ม **ข้อมูล** รายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="9b29f-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="9b29f-165">ตัวเลือกสำหรับ **ข้อมูล** ไม่ปรากฏในรายการแบบหล่นลงด้านล่าง **รายการใบสั่งใหม่**</span><span class="sxs-lookup"><span data-stu-id="9b29f-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="9b29f-166">นี่เกิดขึ้นเนื่องจากมีการติดตั้งการดำเนินงานโครงการในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="9b29f-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="9b29f-167">เมื่อต้องการเปิดใช้งานตัวเลือกฟอร์ม **ข้อมูล** อีกครั้ง ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9b29f-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="9b29f-168">นำทางไปยังเอนทิตี้ **รายการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="9b29f-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="9b29f-169">ค้นหาฟอร์ม **ข้อมูล** ภายใต้โหนดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="9b29f-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="9b29f-170">เลือกฟอร์ม **ข้อมูล** และคลิก **เปิดใช้งานบทบาทความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="9b29f-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="9b29f-171">เปลี่ยนการตั้งค่าความปลอดภัยเป็น **แสดงต่อทุกคน**</span><span class="sxs-lookup"><span data-stu-id="9b29f-171">Change the security setting to **Display to everyone**.</span></span>
