---
title: "รีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล"
description: "หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations"
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="7ca96-103">รีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7ca96-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7ca96-104">หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินหลังจากการคืนค่าฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ca96-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="7ca96-105">ถ้าคุณเคยคืนค่าฐานข้อมูล Finance and Operations ของคุณจากการสำรองข้อมูล หรือคัดลอกฐานข้อมูลจากสภาพแวดล้อมอื่น คุณต้องทำตามขั้นตอนในหัวข้อนี้เพื่อให้แน่ใจว่า Data Mart การรายงานทางการเงินใช้ฐานข้อมูล Finance and Operations ที่คืนค่าได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7ca96-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="7ca96-106">ขั้นตอนในกระบวนการนี้ได้รับการสนับสนุนสำหรับ Dynamics 365 for Operation การนำออกใช้ในเดือนพฤษภาคม 2016 (การสร้างแอพ 7.0.1265.23014 และการสร้างการรายงานทางการเงิน 7.0.10000.4) และการนำออกใช้ที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="7ca96-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="7ca96-107">ถ้าคุณมี Finance and Operations การนำออกใช้ก่อนหน้า ให้ติดต่อทีมสนับสนุนของเราสำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="7ca96-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="7ca96-108">ส่งออกข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ca96-108">Export report definitions</span></span>
<span data-ttu-id="7ca96-109">ก่อนอื่น ให้ส่งออกรูปแบบรายงานที่อยู่ในโปรแกรมออกแบบรายงาน โดยทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7ca96-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="7ca96-110">ในโปรแกรมออกแบบรายงาน ไปที่ **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="7ca96-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="7ca96-111">เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และคลิก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="7ca96-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="7ca96-112">สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="7ca96-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="7ca96-113">เลือกข้อกำหนดของรายงานที่จะส่งออก:</span><span class="sxs-lookup"><span data-stu-id="7ca96-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="7ca96-114">เมื่อต้องการส่งออกข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมดของคุณ คลิก **เลือกทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7ca96-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="7ca96-115">เมื่อต้องการส่งออกรายงาน แถว คอลัมน์ แผนภูมิ หรือเซ็ตมิติที่เฉพาะ คลิกแท็บที่เหมาะสม และจากนั้นเลือกรายการที่จะส่งออก</span><span class="sxs-lookup"><span data-stu-id="7ca96-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="7ca96-116">กดค้างปุ่ม Ctrl เพื่อเลือกหลายรายการในแท็บ เมื่อคุณเลือกรายงานที่จะส่งออก แถว คอลัมน์ ลำดับ หรือชุดมิติที่เกี่ยวข้องจะถูกเลือกด้วย</span><span class="sxs-lookup"><span data-stu-id="7ca96-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="7ca96-117">คลิก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="7ca96-117">Click **Export**.</span></span>
5.  <span data-ttu-id="7ca96-118">ป้อนที่ไฟล์และเลือกตำแหน่งที่ปลอดภัยที่คุณต้องการบันทึกข้อกำหนดของรายงานที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="7ca96-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="7ca96-119">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7ca96-119">Click **Save**.</span></span>

<span data-ttu-id="7ca96-120">สามารถคัดลอกหรืออัปโหลดไฟล์ไปยังตำแหน่งที่ปลอดภัยได้โดยการยินยอมให้นำเข้าไปยังสภาพแวดล้อมอื่นในเวลาอื่น</span><span class="sxs-lookup"><span data-stu-id="7ca96-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="7ca96-121">สามารถดูข้อมูลเกี่ยวกับการใช้บัญชีการจัดเก็บ Microsoft Azure ได้ใน [การถ่ายโอนข้อมูลโดยใช้ยูทิลิตี้บรรทัดคำสั่ง AzCopy](/azure/storage/storage-use-azcopy)</span><span class="sxs-lookup"><span data-stu-id="7ca96-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="7ca96-122">Microsoft ไม่ได้ให้บัญชีการจัดเก็บโดยเป็นส่วนหนึ่งของข้อตกลงของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ca96-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="7ca96-123">คุณต้องซื้อบัญชีการจัดเก็บหรือใช้บัญชีการจัดเก็บจากการสมัครใช้งาน Azure ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="7ca96-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="7ca96-124">ระวังลักษณะการทำงานของไดรฟ์ D บนเครื่องเสมือนของ Azure</span><span class="sxs-lookup"><span data-stu-id="7ca96-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="7ca96-125">อย่าเก็บกลุ่มบล็อคส่วนประกอบที่ส่งออกแล้วของคุณไว้ที่นี่อย่างถาวร</span><span class="sxs-lookup"><span data-stu-id="7ca96-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="7ca96-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไดรฟ์ชั่วคราว ให้ดูที่ [การทำความเข้าใจเกี่ยวกับไดรฟ์ชั่วคราวบนเครื่องเสมือนของ Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</span><span class="sxs-lookup"><span data-stu-id="7ca96-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="7ca96-127">หยุดการบริการ</span><span class="sxs-lookup"><span data-stu-id="7ca96-127">Stop services</span></span>
<span data-ttu-id="7ca96-128">ใช้เดสก์ท็อประยะไกลในการเชื่อมต่อกับคอมพิวเตอร์ทั้งหมดในสภาพแวดล้อมและหยุดการบริการ Windows ต่อไปนี้โดยใช้ services.msc:</span><span class="sxs-lookup"><span data-stu-id="7ca96-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="7ca96-129">บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ AOS ทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="7ca96-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="7ca96-130">การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="7ca96-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="7ca96-131">บริการกระบวนการ Management Reporter 2012 (บนคอมพิวเตอร์ BI เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="7ca96-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="7ca96-132">บริการเหล่านี้จะมีการเชื่อมต่อที่เปิดอยู่กับฐานข้อมูล Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ca96-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="7ca96-133">รีเซ็ต</span><span class="sxs-lookup"><span data-stu-id="7ca96-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="7ca96-134">ค้นหาและดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="7ca96-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="7ca96-135">ค้นหาแพคเกจ MinorVersionDataUpgrade.zip ล่าสุดโดยใช้คำแนะนำที่พบใน [ดาวน์โหลดล่าสุดข้อมูลการอัพเกรดสามารถปรับใช้ได้แพคเกจ](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages)</span><span class="sxs-lookup"><span data-stu-id="7ca96-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="7ca96-136">คำแนะนำอธิบายถึงวิธีการค้นหาและดาวน์โหลดรุ่นที่ถูกต้องของแพคเกจการอัพเกรดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7ca96-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="7ca96-137">ไม่จำเป็นต้องอัพเกรดเพื่อดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="7ca96-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="7ca96-138">คุณเพียงต้องทำตามขั้นตอนในส่วน "ดาวน์โหลดแพคเกจที่สามารถปรับใช้ได้ในการอัพเกรดข้อมูลล่าสุด" โดยไม่ต้องดำเนินขั้นตอนอื่น ๆ ในบทความเพื่อดึงข้อมูลสำเนาของแพคเกจ MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="7ca96-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="7ca96-139">เรียกใช้สคริปต์กับฐานข้อมูล Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ca96-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="7ca96-140">เรียกใช้สคริปต์ต่อไปนี้เทียบกับฐานข้อมูล Finance and Operations (ไม่ใช่เทียบกับฐานข้อมูลการรายงานทางการเงิน)</span><span class="sxs-lookup"><span data-stu-id="7ca96-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="7ca96-141">DataUpgrade.zip\\AosService\\สคริปต์\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="7ca96-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="7ca96-142">DataUpgrade.zip\\AosService\\สคริปต์\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="7ca96-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="7ca96-143">สคริปต์เหล่านี้ทำให้แน่ใจว่าการตั้งค่าการติดตามการเปลี่ยนแปลง บทบาท และผู้ใช้ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7ca96-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="7ca96-144">ดำเนินการคำสั่ง PowerShell เพื่อรีเซ็ตฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7ca96-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="7ca96-145">บนคอมพิวเตอร์ AOS ดำเนินการคำสั่งต่อไปนี้ใน PowerShell โดยเป็นผู้ดูแลระบบเพื่อรีเซ็ตการรวมระหว่าง Finance and Operations และการรายงานทางการเงิน:</span><span class="sxs-lookup"><span data-stu-id="7ca96-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="7ca96-146">หลังจากดำเนินการคำสั่ง คุณจะถูกขอให้ป้อน "Y" เพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="7ca96-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="7ca96-147">คำอธิบายของพารามิเตอร์:</span><span class="sxs-lookup"><span data-stu-id="7ca96-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="7ca96-148">ค่าที่ถูกต้องสำหรับเหตุผลคือ: SERVICING, BADDATA, OTHER</span><span class="sxs-lookup"><span data-stu-id="7ca96-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="7ca96-149">พารามิเตอร์ -ReasonDetail เป็นข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="7ca96-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="7ca96-150">เหตุผลและ reasonDetail จะถูกบันทึกในการตรวจสอบ telemetry/environment</span><span class="sxs-lookup"><span data-stu-id="7ca96-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="7ca96-151">เริ่มการบริการ</span><span class="sxs-lookup"><span data-stu-id="7ca96-151">Start services</span></span>
<span data-ttu-id="7ca96-152">ใช้ services.msc เพื่อเริ่มการทำงานของบริการที่คุณหยุดการทำงานก่อนหน้านี้ใหม่:</span><span class="sxs-lookup"><span data-stu-id="7ca96-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="7ca96-153">บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ AOS ทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="7ca96-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="7ca96-154">การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="7ca96-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="7ca96-155">บริการกระบวนการ Management Reporter 2012 (บนคอมพิวเตอร์ BI เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="7ca96-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="7ca96-156">นำเข้าข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ca96-156">Import report definitions</span></span>
<span data-ttu-id="7ca96-157">นำเข้าการออกแบบรายงานของคุณจากโปรแกรมออกแบบรายงานโดยใช้ไฟล์ที่สร้างขึ้นระหว่างการส่งออก:</span><span class="sxs-lookup"><span data-stu-id="7ca96-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="7ca96-158">ในโปรแกรมออกแบบรายงาน ไปที่ **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="7ca96-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="7ca96-159">เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และคลิก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="7ca96-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="7ca96-160">สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="7ca96-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="7ca96-161">เลือกบล็อคส่วนประกอบ **เริ่มต้น** และคลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="7ca96-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="7ca96-162">เลือกไฟล์ที่ประกอบด้วยข้อกำหนดของรายงานที่ส่งออก แล้วคลิก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="7ca96-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="7ca96-163">ในกล่องโต้ตอบ นำเข้า เลือกข้อกำหนดของรายงานที่จะนำเข้า:</span><span class="sxs-lookup"><span data-stu-id="7ca96-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="7ca96-164">เมื่อต้องการนำเข้าข้อกำหนดของรายงานและบล็อคส่วนประกอบสนับสนุนทั้งหมด คลิก **เลือกทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7ca96-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="7ca96-165">การนำเข้ารายงาน แถว คอลัมน์ แผนภูมิ หรือ เซ็ตมิติที่เฉพาะ ให้เลือกรายงาน แถว คอลัมน์ แผนภูมิ หรือเซ็ตมิติที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="7ca96-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="7ca96-166">คลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="7ca96-166">Click **Import**.</span></span>





