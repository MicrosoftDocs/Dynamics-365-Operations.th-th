---
title: ตั้งค่าคอนฟิกการรวมกับ Dayforce
description: การรวมระหว่าง Microsoft Dynamics 365 Human Resources และ Ceridian Dayforce ขึ้นอยู่กับขั้นตอนการตั้งค่าคอนฟิกหลายขั้นตอนที่อธิบายไว้ในบทความนี้ คุณต้องตั้งค่าคอนฟิกการรวมทั้งในทรัพยากรบุคคลและ Dayforce ก่อนที่คุณจะสามารถประมวลผลรันการจ่ายเงิน
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890015"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="efc51-104">ตั้งค่าคอนฟิกการรวมกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="efc51-105">การรวมระหว่าง Microsoft Dynamics 365 Human Resources และ Ceridian Dayforce ขึ้นอยู่กับขั้นตอนการตั้งค่าคอนฟิกหลายขั้นตอนที่อธิบายไว้ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="efc51-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="efc51-106">คุณต้องตั้งค่าคอนฟิกการรวมทั้งในทรัพยากรบุคคลและ Dayforce ก่อนที่คุณจะสามารถประมวลผลรันการจ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="efc51-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="efc51-107">เมื่อคุณใช้บริการ เช่น Dayforce เพื่อทำให้รันการจ่ายเงินให้เสร็จสมบูรณ์ คุณต้องเปิดใช้งานการรวมในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="efc51-108">การรวมจำเป็นต้องมีข้อมูลที่เฉพาะเจาะจงจากทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="efc51-109">ดังนั้น คุณต้องตรวจสอบว่าข้อมูลที่มีการแม็ปกับ Dayforce ถูกตั้งค่าคอนฟิกในทรัพยากรบุคคลในลักษณะที่สนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="efc51-110">การรวมใช้ประเภทที่กว้างของข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="efc51-111">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-111">Human resources data</span></span>
- <span data-ttu-id="efc51-112">ข้อมูลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-112">Compensation data</span></span>
- <span data-ttu-id="efc51-113">ข้อมูลค่าจ้าง เช่น รอบการชำระค่าจ้าง รอบระยะเวลาการชำระค่าจ้าง และรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="efc51-114">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-114">Worker data</span></span>

<span data-ttu-id="efc51-115">บทความนี้อธิบายขั้นตอนต่างๆ ที่คุณต้องปฏิบัติตามเพื่อเปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="efc51-116">นอกจากนี้ ยังอธิบายถึงชนิดของข้อมูลและรายละเอียดการตั้งค่าคอนฟิกที่การรวมต้องการ</span><span class="sxs-lookup"><span data-stu-id="efc51-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="efc51-117">เปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-117">Enable the integration</span></span>

<span data-ttu-id="efc51-118">ในทรัพยากรบุคคล คุณต้องเปิดใช้งานการรวมและป้อนข้อมูลการตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="efc51-119">ถ้าคุณต้องการธุรกรรมบัญชีแยกประเภททั่วไปที่ถูกผลิตให้ถูกนำเข้าลงใน Microsoft Dynamics 365 Finance คุณยังต้องตั้งค่าบัญชีที่จัดเก็บ Microsoft Azure และป้อนสตริงการเชื่อมต่อที่จัดเก็บ Azure ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="efc51-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="efc51-120">เมื่อต้องการเปิดใช้งานการรวมในในทรัพยากรบุคคล ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="efc51-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="efc51-121">ในหน้า **การดูแลระบบ** เลือก **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="efc51-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="efc51-122">ป้อนปลายทาง File Transfer Protocol (FTP) แบบปลอดภัย และพาธโฟลเดอร์ FTP แบบปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="efc51-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="efc51-123">ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่จะเข้าถึงปลายทาง FTP แบบปลอดภัย และโฟลเดอร์พาธ</span><span class="sxs-lookup"><span data-stu-id="efc51-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="efc51-124">ทดสอบการเชื่อมต่อ หากจำเป็น และตั้งค่าตัวเลือก **เปิดใช้งานการรวมค่าจ้าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="efc51-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="efc51-125">เมื่อเปิดการรวม มีการสร้างแพคเกจการส่งออกข้อมูลและไฟล์ และมีการตั้งค่าความถี่</span><span class="sxs-lookup"><span data-stu-id="efc51-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="efc51-126">คุณสามารถเปลี่ยนความถี่นี้ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="efc51-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="efc51-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบัญชีการจัดเก็บ Azure และสตริงการเชื่อมต่อการจัดเก็บ Azure ให้ดูบทความ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="efc51-128">เกี่ยวกับบัญชีการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="efc51-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="efc51-129">ตั้งค่าคอนฟิกสตริงการเชื่อมต่อการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="efc51-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="efc51-130">รายละเอียดทางเทคนิค เมื่อเปิดใช้งานการรวมค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="efc51-131">การเปิดการรวมค่าจ้างมีผลกระทบหลักสองประการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="efc51-132">โครงการส่งออกข้อมูลที่มีชื่อว่า "การส่งออกการรวมค่าจ้าง" ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="efc51-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="efc51-133">โครงการนี้ประกอบด้วยเอนทิตีและฟิลด์ที่จำเป็นสำหรับการรวมค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="efc51-134">เมื่อต้องการตรวจสอบโครงการ ให้ไปที่ **การจัดการระบบ** เลือกไทล์ **การจัดการข้อมูล** แล้วเปิดโครงการข้อมูลจากรายการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="efc51-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="efc51-135">ชุดงานนี้จะดำเนินการโครงการส่งออกข้อมูล เข้ารหัสแพคเกจข้อมูลที่เป็นผลลัพธ์ และโอนย้ายไฟล์แพคเกจข้อมูลไปยังปลายทาง SFTP ที่ตั้งค่าคอนฟิกบนหน้าจอ **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="efc51-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="efc51-136">แพคเกจข้อมูลที่โอนย้ายไปยังปลายทาง SFTP ถูกเข้ารหัสโดยใช้คีย์ที่ไม่ซ้ำกันสำหรับแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="efc51-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="efc51-137">คีย์อยู่ใน Azure Key Vault ที่สามารถเข้าถึงได้โดย Ceridian เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="efc51-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="efc51-138">ไม่สามารถถอดรหัสและตรวจสอบเนื้อหาของแพคเกจข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="efc51-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="efc51-139">ถ้าคุณต้องการตรวจสอบเนื้อหาของแพคเกจข้อมูล คุณต้องส่งออกโครงการข้อมูล "การส่งออกการรวมบัญชีค่าจ้าง" ด้วยตนเอง ให้ดาวน์โหลดโครงการนั้น แล้วเปิด</span><span class="sxs-lookup"><span data-stu-id="efc51-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="efc51-140">การส่งออกด้วยตนเองจะไม่ใช้การเข้ารหัสหรือโอนย้ายบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="efc51-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="efc51-141">ตัวอย่างเช่นที่ไฟล์การรวมถูกส่งจากสภาพแวดล้อม UAT Dynamics 365 Human Resources หรือ Sandbox ไปยังสภาพแวดล้อมการทดสอบ Ceridian Dayforce คุณสามารถใช้ URL ของ Key Vault ต่อไปนี้: https://payrollintegrationprod.vault.azure.net</span><span class="sxs-lookup"><span data-stu-id="efc51-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="efc51-142">ตั้งค่าคอนฟิกข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="efc51-142">Configure your data</span></span> 

<span data-ttu-id="efc51-143">ในการประมวลผลค่าจ้าง คุณต้องตั้งค่าคอนฟิกข้อมูลทรัพยากรบุคคลในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="efc51-144">คุณต้องตั้งค่าข้อมูลองค์กร เช่น งาน และตำแหน่ง พร้อมด้วยข้อมูลค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="efc51-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="efc51-145">ข้อมูลนี้ให้ข้อมูลการจ้างงาน ค่าจ้าง และการหักลด ที่จำเป็นในการสร้างค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="efc51-146">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="efc51-147">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="efc51-147">Benefits</span></span> 

<span data-ttu-id="efc51-148">ทรัพยากรบุคคลให้เครื่องมือสำหรับการตั้งค่าและการบำรุงรักษาของสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงาน ที่หน่วยงานนำเสนอหรือประมวลผลสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="efc51-149">เมื่อคุณสร้างสวัสดิการ พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="efc51-150">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="efc51-150">Benefit plans</span></span>

- <span data-ttu-id="efc51-151">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-151">Plan (required)</span></span>
- <span data-ttu-id="efc51-152">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-152">Type (required)</span></span>
- <span data-ttu-id="efc51-153">ผลกระทบของค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-153">Payroll impact (required)</span></span>
- <span data-ttu-id="efc51-154">ขอคืนเงินค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="efc51-154">Recover arrears</span></span>
- <span data-ttu-id="efc51-155">วิธีการหักลด</span><span class="sxs-lookup"><span data-stu-id="efc51-155">Deduction method</span></span>
- <span data-ttu-id="efc51-156">ระดับความสำคัญการหักลด</span><span class="sxs-lookup"><span data-stu-id="efc51-156">Deduction priority</span></span>
- <span data-ttu-id="efc51-157">จำกัดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="efc51-157">Limit period</span></span>
- <span data-ttu-id="efc51-158">ยอดวงเงิน</span><span class="sxs-lookup"><span data-stu-id="efc51-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="efc51-159">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="efc51-159">Benefits</span></span>

- <span data-ttu-id="efc51-160">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-160">Plan (required)</span></span>
- <span data-ttu-id="efc51-161">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-161">Type (required)</span></span>
- <span data-ttu-id="efc51-162">ตัวเลือก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-162">Option (required)</span></span>
- <span data-ttu-id="efc51-163">รหัสสวัสดิการ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-163">Benefit ID (required)</span></span>
- <span data-ttu-id="efc51-164">ความถี่</span><span class="sxs-lookup"><span data-stu-id="efc51-164">Frequency</span></span>
- <span data-ttu-id="efc51-165">ข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="efc51-165">Basis</span></span>
- <span data-ttu-id="efc51-166">ยอดเงินหรืออัตรา</span><span class="sxs-lookup"><span data-stu-id="efc51-166">Amount or rate</span></span>
- <span data-ttu-id="efc51-167">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="efc51-168">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="efc51-168">Supported frequencies</span></span> 

- <span data-ttu-id="efc51-169">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="efc51-169">Weekly</span></span>
- <span data-ttu-id="efc51-170">ทุกสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="efc51-170">Bi-weekly</span></span>
- <span data-ttu-id="efc51-171">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-171">Semi-monthly</span></span>
- <span data-ttu-id="efc51-172">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="efc51-173">ฐานที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="efc51-173">Supported bases</span></span> 

- <span data-ttu-id="efc51-174">ยอดเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="efc51-174">Fixed amount</span></span>
- <span data-ttu-id="efc51-175">เปอร์เซ็นต์ของรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-175">Percent of earnings</span></span>
- <span data-ttu-id="efc51-176">ชั่วโมงที่มีประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-176">Productive hours</span></span>

<span data-ttu-id="efc51-177">Dayforce สร้างการหักลดต่อไปนี้ โดยขึ้นอยู่กับผลกระทบของค่าจ้างที่กำหนดในแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="efc51-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="efc51-178">การเลือกในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-178">Selection in Human Resources</span></span>        | <span data-ttu-id="efc51-179">ผลลัพธ์ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="efc51-180">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="efc51-180">None</span></span>                       | <span data-ttu-id="efc51-181">ไม่มีการสร้างการหักลด</span><span class="sxs-lookup"><span data-stu-id="efc51-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="efc51-182">การหักลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="efc51-182">Deduction only</span></span>             | <span data-ttu-id="efc51-183">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="efc51-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="efc51-184">การจ่ายเงินสมทบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="efc51-184">Contribution only</span></span>          | <span data-ttu-id="efc51-185">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="efc51-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="efc51-186">การหักลดและการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="efc51-186">Deduction and contribution</span></span> | <span data-ttu-id="efc51-187">การหักลดพนักงานและนายจ้างจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="efc51-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="efc51-188">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดและจัดการโปรแกรมสวัสดิการ ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="efc51-189">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="efc51-190">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="efc51-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="efc51-191">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="efc51-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="efc51-192">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="efc51-193">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-193">Compensation</span></span> 

<span data-ttu-id="efc51-194">การจัดการค่าตอบแทนจะใช้ควบคุมการจัดส่งของค่าจ้างพื้นฐานและเงินรางวัล</span><span class="sxs-lookup"><span data-stu-id="efc51-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="efc51-195">ค่าจ้างพื้นฐานคงที่ของพนักงานและการขึ้นค่าตอบแทนตามผลงานจะถูกควบคุมโดยใช้แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="efc51-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="efc51-196">ค่าจ้างจูงใจเช่นการชำระเงินโบนัส รางวัลตามผลการปฏิบัติงาน สิทธิในการซื้อหุ้น การให้หุ้น รางวัลที่จ่ายครั้งเดียว โดยใช้แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="efc51-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="efc51-197">Dayforce ใช้ข้อมูลค่าตอบแทนที่คำนวณอัตรารายชั่วโมงหรือรายปีของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="efc51-198">จำเป็นต้องมีแผนค่าตอบแทนคงที่และการแปลงอัตราค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="efc51-199">พนักงานต้องเชื่อมโยงกับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="efc51-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="efc51-200">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแผนค่าตอบแทน โปรดดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="efc51-201">สร้างแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="efc51-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="efc51-202">สร้างแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="efc51-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="efc51-203">พัฒนาโครงสร้างและแผนเงินเดือน/ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="efc51-204">ประมวลผลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="efc51-205">กำหนดกระบวนการของค่าตอบแทนและคำนวณผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="efc51-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="efc51-206">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="efc51-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="efc51-207">การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="efc51-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="efc51-208">งาน</span><span class="sxs-lookup"><span data-stu-id="efc51-208">Jobs</span></span> 

<span data-ttu-id="efc51-209">งานเป็นชุดของงานและความรับผิดชอบที่ถูกระบุของบุคคลที่ดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="efc51-210">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="efc51-211">การตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="efc51-212">กำหนดงานใหม่</span><span class="sxs-lookup"><span data-stu-id="efc51-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="efc51-213">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-213">Positions</span></span>

<span data-ttu-id="efc51-214">ตำแหน่งคือแต่ละอินสแตนซ์ของงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="efc51-215">ตัวอย่างเช่น ตำแหน่ง "ผู้จัดการฝ่ายขาย (ตะวันออก)" เป็นหนึ่งในตำแหน่งที่เชื่อมโยงกับงาน "ผู้จัดการฝ่ายขาย"</span><span class="sxs-lookup"><span data-stu-id="efc51-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="efc51-216">ตำแหน่งมีอยู่ในแผนก</span><span class="sxs-lookup"><span data-stu-id="efc51-216">A position exists in a department.</span></span> <span data-ttu-id="efc51-217">สามารถเชื่อมโยงผู้ปฏิบัติงานหนึ่งรายกับแต่ละตำแหน่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="efc51-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="efc51-218">เก็บข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ไว้ เมื่อคุณตั้งค่าตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="efc51-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="efc51-219">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-219">Position (required)</span></span>
- <span data-ttu-id="efc51-220">คำอธิบาย (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-220">Description (required)</span></span>
- <span data-ttu-id="efc51-221">งาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-221">Job (required)</span></span>
- <span data-ttu-id="efc51-222">แผนก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-222">Department (required)</span></span>
- <span data-ttu-id="efc51-223">ชนิดตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-223">Position type (required)</span></span>
- <span data-ttu-id="efc51-224">จำนวนบุคลากรเทียบเท่าเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="efc51-224">Full-time equivalent</span></span>
- <span data-ttu-id="efc51-225">ชั่วโมงปกติรายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="efc51-226">ชำระโดยนิติบุคคล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="efc51-227">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-227">Pay cycle (required)</span></span>
- <span data-ttu-id="efc51-228">มิติทางการเงินเริ่มต้น – ศูนย์ต้นทุน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="efc51-229">การมอบหมายผู้ปฏิบัติงาน – ผู้ปฏิบัติงาน การเริ่มต้นการกำหนด การสิ้นสุดการกำหนด รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="efc51-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="efc51-230">ถ้าตำแหน่งหลายตำแหน่งในแผนกเดียวกันเกี่ยวข้องกับงานเดียวกัน จะมีการรวมลงในตำแหน่งหนึ่งๆ ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="efc51-231">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="efc51-232">จัดระเบียบบุคลากรของคุณโดยใช้แผนก งาน และตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="efc51-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="efc51-233">ตั้งค่าตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="efc51-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="efc51-234">แผนก</span><span class="sxs-lookup"><span data-stu-id="efc51-234">Departments</span></span>

<span data-ttu-id="efc51-235">แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="efc51-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="efc51-236">แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="efc51-237">คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="efc51-238">แผนกอาจมีความรับผิดชอบกำไรและขาดทุน</span><span class="sxs-lookup"><span data-stu-id="efc51-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="efc51-239">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="efc51-240">สร้างแผนกและการเชื่อมโยงกับลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="efc51-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="efc51-241">กำหนดฝ่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="efc51-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="efc51-242">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="efc51-243">รอบการชำระค่าจ้างกำหนดความถี่ในการรันค่าจ้าง และจำนวนวันที่เจาะจงเมื่อผู้ปฏิบัติงานได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="efc51-244">ตัวอย่างเช่น รอบการชำระค่าจ้างอาจเป็นรายเดือน และพนักงานอาจได้รับค่าจ้างในวันสุดท้ายของเดือนนั้น</span><span class="sxs-lookup"><span data-stu-id="efc51-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="efc51-245">อีกทางหนึ่งคือ รอบการชำระค่าจ้างอาจเป็นรายสัปดาห์ และพนักงานอาจได้รับค่าจ้างในวันอังคารหลังจากจุดสิ้นสุดของรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="efc51-246">รอบการชำระค่าจ้างถูกกำหนดให้กับตำแหน่ง เพื่อควบคุมเวลาที่ผู้ปฏิบัติงานในตำแหน่งเหล่านั้นได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="efc51-247">หลังจากที่คุณสร้างรอบการชำระค่าจ้าง คุณสามารถสร้างรอบระยะเวลาการชำระค่าจ้างสำหรับแต่ละรอบได้</span><span class="sxs-lookup"><span data-stu-id="efc51-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="efc51-248">รอบการชำระค่าจ้างแต่ละรอบรวมถึงวันที่ของการชำระเงินเริ่มต้นที่ยึดตามข้อมูลที่คุณให้</span><span class="sxs-lookup"><span data-stu-id="efc51-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="efc51-249">อย่างไรก็ตาม คุณสามารถแก้ไขวันที่การชำระเงินเริ่มต้นได้ในรอบการชำระค่าจ้างเพื่อให้อนุญาตการยกเว้น เช่น เมื่อวันที่ชำระเงินตรงกับวันหยุด</span><span class="sxs-lookup"><span data-stu-id="efc51-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="efc51-250">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="efc51-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="efc51-251">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-251">Pay cycle (required)</span></span>
- <span data-ttu-id="efc51-252">ความถี่ของรอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="efc51-253">วันที่เริ่มรอบระยะเวลา (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="efc51-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="efc51-254">วันที่การชำระเงินเริ่มต้น (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="efc51-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="efc51-255">ข้อมูลนี้ถูกรวมเข้ากับ Dayforce เป็นกลุ่มค่าจ้าง และจะถูกแยกตามประเทศหรือภูมิภาคสำหรับรอบการชำระค่าจ้างแต่ละรอบ</span><span class="sxs-lookup"><span data-stu-id="efc51-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="efc51-256">ต้องมีการสร้างรอบระยะเวลาการชำระค่าจ้างอย่างน้อยหนึ่งรายการ ก่อนที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="efc51-257">Dayforce สร้างปฏิทินกลุ่มค่าจ้างและวันที่ในการชำระเงิน โดยยึดตามวันที่เริ่มต้นของรอบระยะเวลาการชำระค่าจ้างแรก และวันที่ชำระเงินเริ่มต้นที่ตั้งค่าในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="efc51-258">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-258">Earning codes</span></span>

<span data-ttu-id="efc51-259">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="efc51-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="efc51-260">รหัสมีพารามิเตอร์ต่าง ๆ ที่เกี่ยวข้องกับรายได้ เช่น แต่ละ กฎทางบัญชี กฎภาษี และรายงานความต้องการและความสามารถในการรวมได้</span><span class="sxs-lookup"><span data-stu-id="efc51-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="efc51-261">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="efc51-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="efc51-262">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-262">Earning Code (required)</span></span>
- <span data-ttu-id="efc51-263">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-263">Description</span></span>
- <span data-ttu-id="efc51-264">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="efc51-264">Unit of measure</span></span>
- <span data-ttu-id="efc51-265">ประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="efc51-266">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-266">Worker data</span></span>

<span data-ttu-id="efc51-267">เรกคอร์ดสำหรับชนิดต่างๆ ของผู้ปฏิบัติงานที่คุณมี มีความสำคัญสำหรับระบบค่าจ้างและทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="efc51-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="efc51-268">ข้อมูลที่คุณป้อนสามารถใช้ติดตามผู้ปฏิบัติงานและข้อมูลส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="efc51-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="efc51-269">คุณสามารถรักษาข้อมูลต่อไปนี้สำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="efc51-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="efc51-270">**พื้นฐาน** – รักษาข้อมูลพื้นฐานเกี่ยวกับผู้ปฏิบัติงาน เช่น ข้อมูลการติดต่อ ข้อมูลทางประชากรศาสตร์ ข้อมูลการระบุรหัสประจำตัว ข้อมูลครอบครัว สถานะการรับราชการทหาร ข้อมูลคนต่างด้าว และผู้ติดต่อได้ในกรณีฉุกเฉินและส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="efc51-271">**การจ้างงาน** – รักษาข้อมูลเกี่ยวกับการจ้างงานของผู้ปฏิบัติงาน เช่น บริษัท หรือสังกัดองค์กร การมอบหมายตำแหน่งงาน วันที่เริ่มต้นและสิ้นสุด สิทธิการทำงาน เงื่อนไขในการจ้างงาน เงินบำนาญ วันหยุดพักผ่อน และข้อมูลการย้ายสถานที่</span><span class="sxs-lookup"><span data-stu-id="efc51-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="efc51-272">**การลางานและการขาดงาน** – รักษาข้อมูลเกี่ยวกับการขาดงานของผู้ปฏิบัติงาน เช่น ปฏิทินการทำงาน ธุรกรรมการขาดงาน และการตั้งค่าการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="efc51-273">**ค่าตอบแทนและค่าจ้าง** – รักษาข้อมูลเกี่ยวกับแผนค่าตอบแทนของผู้ปฏิบัติงานและข้อมูลค่าจ้าง เช่น การลงทะเบียนสำหรับแผน รางวัล ประสิทธิภาพ ค่าคอมมิชชัน ข้อมูลภาษี การเกษียณอายุ และการหักเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="efc51-274">เมื่อคุณป้อนข้อมูลผู้ปฏิบัติงาน พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="efc51-275">ข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="efc51-275">General information</span></span>

- <span data-ttu-id="efc51-276">หมายเลขบุคลากร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-276">Personnel number (required)</span></span>
- <span data-ttu-id="efc51-277">ชื่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-277">First name (required)</span></span>
- <span data-ttu-id="efc51-278">นามสกุล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-278">Last name (required)</span></span>
- <span data-ttu-id="efc51-279">ชื่อกลาง</span><span class="sxs-lookup"><span data-stu-id="efc51-279">Middle name</span></span>
- <span data-ttu-id="efc51-280">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-280">Seniority date</span></span>
- <span data-ttu-id="efc51-281">เรียกว่า</span><span class="sxs-lookup"><span data-stu-id="efc51-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="efc51-282">ข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-282">Personal information</span></span>

- <span data-ttu-id="efc51-283">สถานภาพการสมรส (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-283">Marital status (required)</span></span>
- <span data-ttu-id="efc51-284">วันที่เกิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-284">Birth date (required)</span></span>
- <span data-ttu-id="efc51-285">เพศ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-285">Gender (required)</span></span>
- <span data-ttu-id="efc51-286">บุคคลทุพพลภาพ</span><span class="sxs-lookup"><span data-stu-id="efc51-286">Person with disabilities</span></span>
- <span data-ttu-id="efc51-287">สัญชาติประเทศภูมิภาค (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="efc51-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="efc51-288">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="efc51-288">Address information</span></span>

- <span data-ttu-id="efc51-289">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-289">Primary (required)</span></span>
- <span data-ttu-id="efc51-290">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-290">Country/region (required)</span></span>
- <span data-ttu-id="efc51-291">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-291">Postal code (required)</span></span>
- <span data-ttu-id="efc51-292">หมายเลขถนน (จำเป็น) (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="efc51-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="efc51-293">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="efc51-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="efc51-294">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-294">City (required)</span></span>
- <span data-ttu-id="efc51-295">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-295">State (required)</span></span>
- <span data-ttu-id="efc51-296">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="efc51-297">ข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="efc51-297">Contact information</span></span> 

- <span data-ttu-id="efc51-298">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-298">Primary (required)</span></span>
- <span data-ttu-id="efc51-299">หมายเลขผู้ติดต่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-299">Contact number (required)</span></span>
- <span data-ttu-id="efc51-300">การขยาย</span><span class="sxs-lookup"><span data-stu-id="efc51-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="efc51-301">ข้อมูลค่าจ้างและรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-301">Payroll information and earning codes</span></span>

<span data-ttu-id="efc51-302">พนักงานอาจถูกกำหนดรายได้เฉพาะที่ความถี่ที่กำหนดของการชำระเงิน และมีวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="efc51-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="efc51-303">ฟิลด์ต่อไปนี้จะใช้ใน Dayforce เพื่อช่วยในการรับประกันว่า การกำหนดลักษณะและการตั้งค่าเหล่านั้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="efc51-304">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-304">Earning codes</span></span>

- <span data-ttu-id="efc51-305">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-305">Position (required)</span></span>
- <span data-ttu-id="efc51-306">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-306">Earning Code (required)</span></span>
- <span data-ttu-id="efc51-307">ความถี่ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-307">Frequency (required)</span></span>
- <span data-ttu-id="efc51-308">จำนวน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="efc51-309">ข้อมูลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-309">Payroll information</span></span>

- <span data-ttu-id="efc51-310">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="efc51-310">Payment Method</span></span>
- <span data-ttu-id="efc51-311">ภูมิภาคเศรษฐกิจ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-311">Economic Region (required)</span></span>
- <span data-ttu-id="efc51-312">รหัสสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-312">Employee Benefits ID</span></span>
- <span data-ttu-id="efc51-313">หมายเลขรหัสประจำชาติ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-313">National ID Number (required)</span></span>
- <span data-ttu-id="efc51-314">หมายเลขการรับราชการทหาร</span><span class="sxs-lookup"><span data-stu-id="efc51-314">Military Service Number</span></span>
- <span data-ttu-id="efc51-315">รหัสกะ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-315">Shift ID (required)</span></span>
- <span data-ttu-id="efc51-316">หมายเลขภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-316">Tax Number (required)</span></span>
- <span data-ttu-id="efc51-317">รหัสสหภาพ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-317">Union ID (required)</span></span>
- <span data-ttu-id="efc51-318">รหัสวันทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-318">Work Day ID (required)</span></span>
- <span data-ttu-id="efc51-319">หมายเลขใบอนุญาตทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="efc51-320">สำหรับวิธีการชำระเงิน เม็กซิโกสนับสนุน **เงินสด** **เช็ค** (เช็คจริงของบริษัท) และ **การชำระเงินทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="efc51-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="efc51-321">ถ้าไม่มีการระบุวิธีการชำระเงิน **เช็ค** จะถูกใช้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="efc51-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="efc51-322">รายละเอียดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-322">Employment details</span></span>

<span data-ttu-id="efc51-323">ประวัติรายละเอียดตการจ้างงานถูกใช้เป็นข้อมูลสำคัญในการสืบทอดการพนักงานจ้างงานของพนักงาน การหยุดชะงัก และสถานะการจ้างงานใหม่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="efc51-324">Dayforce สนับสนุนเรกคอร์ดการจ้างงานที่ใช้งานอยู่เพียงรายการเดียวในแต่ละครั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="efc51-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="efc51-325">วันที่เริ่มต้นการจ้างงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-325">Employment start date (required)</span></span>
- <span data-ttu-id="efc51-326">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-326">Employment end date</span></span>
- <span data-ttu-id="efc51-327">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="efc51-327">Start date</span></span>
- <span data-ttu-id="efc51-328">วันที่เริ่มต้นที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="efc51-328">Adjusted start date</span></span>
- <span data-ttu-id="efc51-329">วันที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="efc51-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="efc51-330">เหตุผลที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="efc51-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="efc51-331">วันสำคัญของพนักงานได้รับมาโดยใช้ข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="efc51-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="efc51-332">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-332">Human Resources</span></span>                | <span data-ttu-id="efc51-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc51-334">วันที่จ้างงานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="efc51-334">Most recent hire date</span></span> | <span data-ttu-id="efc51-335">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="efc51-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="efc51-336">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-336">Termination date</span></span>      | <span data-ttu-id="efc51-337">วันที่สิ้นสุดการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="efc51-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="efc51-338">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="efc51-338">Start date</span></span>            | <span data-ttu-id="efc51-339">วันที่เริ่มต้นที่ปรับปรุงแล้ว วันที่เริ่มต้น หรือการเริ่มต้นการจ้างงานของเรกคอร์ประวัติการจ้างงานที่ไม่ได้ใช้งานอยู่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="efc51-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="efc51-340">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="efc51-340">Original hire date</span></span>    | <span data-ttu-id="efc51-341">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานแรกสุด</span><span class="sxs-lookup"><span data-stu-id="efc51-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="efc51-342">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-342">Compensation</span></span>

<span data-ttu-id="efc51-343">แผนค่าตอบแทนคงต้องเชื่อมโยงกับตำแหน่งหลักของพนักงานทุกตำแหน่ง ตลอดรอบระยะเวลาการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="efc51-344">รอบระยะเวลานี้เริ่มต้นในวันที่ที่พนักงานถูกจ้างงาน (หรือวันที่เริ่มต้นการจ้างงาน) และดำเนินต่อไปจนกว่าจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="efc51-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="efc51-345">วันที่มีผลบังคับใช้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-345">Effective Date (required)</span></span>
- <span data-ttu-id="efc51-346">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="efc51-346">Expiration date</span></span>
- <span data-ttu-id="efc51-347">อัตราการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-347">Pay Rate (required)</span></span>
- <span data-ttu-id="efc51-348">การแปลงอัตราค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="efc51-349">จำนวนเทียบเท่ารายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="efc51-350">จำนวนเทียบเท่ารายชั่วโมง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="efc51-351">ถ้าพนักงานรายชั่วโมงมีตำแหน่งหลายตำแหน่ง ค่าตอบแทนคงที่ของตำแหน่งหลักจะถูกนำเข้าใน Dayforce เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="efc51-352">สำหรับตำแหน่งที่ไม่ใช่ตำแหน่งหลัก อัตรารายชั่วโมงถูกบันทึกลงในตำแหน่งที่สอดคล้องกันใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="efc51-353">ถ้าพนักงานประจำมีตำแหน่งหลายตำแหน่ง จะได้รับอัตราชั่วโมงสะสมและเงินเดือนต่อปีระหว่างตำแหน่งที่ใช้งานอยู่ทั้งหมด และถูกใช้เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="efc51-354">หมายเลขรหัส</span><span class="sxs-lookup"><span data-stu-id="efc51-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="efc51-355">ตัวระบุประกันสังคม</span><span class="sxs-lookup"><span data-stu-id="efc51-355">Social Security identifier</span></span> 

<span data-ttu-id="efc51-356">พนักงานทุกคนต้องมีตัวระบุหลักหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="efc51-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="efc51-357">ตัวระบุนี้ต้องเป็นชนิดรหัส **SSN**</span><span class="sxs-lookup"><span data-stu-id="efc51-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="efc51-358">ใน Dayforce จะได้รับมาโดยอัตโนมัติเป็นตัวระบุประกันสังคมของพนักงานที่จำเป็นสำหรับการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="efc51-359">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-359">Primary (required)</span></span>
- <span data-ttu-id="efc51-360">ชนิดข้อมูลประจำตัว = "SSN"</span><span class="sxs-lookup"><span data-stu-id="efc51-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="efc51-361">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="efc51-361">Issued Date</span></span>
- <span data-ttu-id="efc51-362">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="efc51-362">Expiration Date</span></span>

<span data-ttu-id="efc51-363">พนักงานสามารถประกาศหมายเลขการระบุรหัสประจำตัวหลายเลขของชนิดการระบุรหัสประจำตัว **SSN**</span><span class="sxs-lookup"><span data-stu-id="efc51-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="efc51-364">อย่างไรก็ตาม เฉพาะเรกคอร์ดที่ถูกทำเครื่องหมายเป็น **หลัก** ถูกรวมเข้ากับ Dayforce ไม่ว่าหมายเลขจะใช้งานอยู่ หรือหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="efc51-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="efc51-365">บัญชีธนาคารและการเบิกจ่าย</span><span class="sxs-lookup"><span data-stu-id="efc51-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="efc51-366">ต้องป้อนข้อมูลบัญชีธนาคารที่ถูกต้องสำหรับพนักงานใดๆ ที่เลือกที่จะรับการชำระเงินผ่านการโอนย้ายของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="efc51-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="efc51-367">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-367">Human Resources</span></span>                         | <span data-ttu-id="efc51-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc51-369">หมายเลขบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="efc51-370">รหัส SWIFT (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-370">SWIFT code (required)</span></span>          | <span data-ttu-id="efc51-371">ฟิลด์ **รหัสธนาคาร** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="efc51-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="efc51-372">หมายเลขสาขา (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="efc51-373">ชนิดของบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-373">Bank account type (required)</span></span>   | <span data-ttu-id="efc51-374">ฟิลด์ **ชนิดของบัญชี** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="efc51-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="efc51-375">ค่าที่ได้รับการสนับสนุนได้แก่ **การตรวจสอบ** และ **ค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="efc51-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="efc51-376">พนักงานที่เลือกจะรับการชำระผ่านการโอนผ่านบัญชีธนาคาร ต้องมีลิงก์ไปยังบัญชีเงินส่วนที่เหลือที่อยู่ภายใต้นิติบุคคลที่มีที่อยู่หลักในเม็กซิโก และเชื่อมโยงกับบัญชีธนาคารที่ถูกต้องจากธนาคารเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="efc51-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="efc51-377">บัญชีที่ไม่ใช่เงินส่วนที่เหลืออื่นๆ ทั้งหมดจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="efc51-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="efc51-378">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="efc51-378">Address information</span></span>

<span data-ttu-id="efc51-379">พนักงานทุกคนต้องมีสถานที่หลักหนึ่งแห่ง</span><span class="sxs-lookup"><span data-stu-id="efc51-379">Every employee must have one primary location.</span></span> <span data-ttu-id="efc51-380">ใน Dayforce สถานที่นี้จะใช้เพื่อกำหนดที่พักอาศัยหลักของพนักงานสำหรับวัตถุประสงค์ด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="efc51-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="efc51-381">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-381">Primary (required)</span></span>
- <span data-ttu-id="efc51-382">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-382">Country/region (required)</span></span>
- <span data-ttu-id="efc51-383">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="efc51-384">ถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-384">Street (required)</span></span>
- <span data-ttu-id="efc51-385">หมายเลขถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-385">Street Number (required)</span></span>
- <span data-ttu-id="efc51-386">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="efc51-386">Building Complement</span></span>
- <span data-ttu-id="efc51-387">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-387">City (required)</span></span>
- <span data-ttu-id="efc51-388">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-388">State (required)</span></span>
- <span data-ttu-id="efc51-389">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="efc51-390">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="efc51-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="efc51-391">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในสหรัฐอเมริกาและแคนาดา ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="efc51-392">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-392">Departments are required on positions.</span></span>
- <span data-ttu-id="efc51-393">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="efc51-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="efc51-394">คุณสามารถตั้งค่าคอนฟิกทรัพยากรบุคคลเพื่อกำหนดว่าตำแหน่งต้องมีการระบุแผนก</span><span class="sxs-lookup"><span data-stu-id="efc51-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="efc51-395">เมื่อต้องการทำเช่นนี้ ไปยัง **ตำแหน่งที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล > ตำแหน่ง > ต้องการแผนกในตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="efc51-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="efc51-396">เราขอแนะนำให้ การตั้งค่านี้ถูกบังคับใช้สำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="efc51-397">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-397">Job types</span></span>

<span data-ttu-id="efc51-398">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="efc51-399">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="efc51-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="efc51-400">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="efc51-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="efc51-401">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="efc51-402">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="efc51-403">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-403">Job type</span></span>   | <span data-ttu-id="efc51-404">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="efc51-405">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="efc51-405">Hourly</span></span>     | <span data-ttu-id="efc51-406">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="efc51-406">Hourly</span></span>      |
| <span data-ttu-id="efc51-407">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-407">Salaried</span></span>   | <span data-ttu-id="efc51-408">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="efc51-409">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-409">Position types</span></span> 

<span data-ttu-id="efc51-410">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="efc51-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="efc51-411">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="efc51-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="efc51-412">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="efc51-413">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="efc51-413">Position type</span></span>   | <span data-ttu-id="efc51-414">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="efc51-415">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="efc51-415">Full-time</span></span>       | <span data-ttu-id="efc51-416">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="efc51-416">Full time employee</span></span> |
| <span data-ttu-id="efc51-417">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="efc51-417">Part-time</span></span>       | <span data-ttu-id="efc51-418">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="efc51-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="efc51-419">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="efc51-419">Reason codes</span></span>

<span data-ttu-id="efc51-420">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="efc51-421">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="efc51-422">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="efc51-423">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="efc51-423">Reason code</span></span>    | <span data-ttu-id="efc51-424">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-424">Description</span></span>      | <span data-ttu-id="efc51-425">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="efc51-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="efc51-426">การลาออก</span><span class="sxs-lookup"><span data-stu-id="efc51-426">RESIGNATION</span></span>    | <span data-ttu-id="efc51-427">การลาออก</span><span class="sxs-lookup"><span data-stu-id="efc51-427">Resignation</span></span>      | <span data-ttu-id="efc51-428">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-428">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-429">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-429">TERMINATION</span></span>    | <span data-ttu-id="efc51-430">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-430">Termination</span></span>      | <span data-ttu-id="efc51-431">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-431">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-432">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="efc51-432">RETIREMENT</span></span>     | <span data-ttu-id="efc51-433">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="efc51-433">Retirement</span></span>       | <span data-ttu-id="efc51-434">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-434">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-435">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-435">OTHER</span></span>          | <span data-ttu-id="efc51-436">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-436">Other Reasons</span></span>    | <span data-ttu-id="efc51-437">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-437">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-438">ความตาย</span><span class="sxs-lookup"><span data-stu-id="efc51-438">DEATH</span></span>          | <span data-ttu-id="efc51-439">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="efc51-439">Death</span></span>            | <span data-ttu-id="efc51-440">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-440">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="efc51-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="efc51-442">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="efc51-442">Leave of Absence</span></span> | <span data-ttu-id="efc51-443">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-443">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="efc51-444">CONTRACTEND</span></span>    | <span data-ttu-id="efc51-445">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="efc51-445">End of Contract</span></span>  | <span data-ttu-id="efc51-446">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-446">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="efc51-447">SALARYCHANGE</span></span>   | <span data-ttu-id="efc51-448">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-448">Change of Salary</span></span> | <span data-ttu-id="efc51-449">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="efc51-450">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="efc51-450">Marital status</span></span>

<span data-ttu-id="efc51-451">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="efc51-452">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="efc51-453">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-453">Human Resources</span></span>                 | <span data-ttu-id="efc51-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="efc51-455">สมรส</span><span class="sxs-lookup"><span data-stu-id="efc51-455">Married</span></span>                | <span data-ttu-id="efc51-456">สมรส</span><span class="sxs-lookup"><span data-stu-id="efc51-456">Married</span></span>              |
| <span data-ttu-id="efc51-457">โสด</span><span class="sxs-lookup"><span data-stu-id="efc51-457">Single</span></span>                 | <span data-ttu-id="efc51-458">โสด</span><span class="sxs-lookup"><span data-stu-id="efc51-458">Single</span></span>               |
| <span data-ttu-id="efc51-459">หม้าย</span><span class="sxs-lookup"><span data-stu-id="efc51-459">Widowed</span></span>                | <span data-ttu-id="efc51-460">หม้าย</span><span class="sxs-lookup"><span data-stu-id="efc51-460">Widowed</span></span>              |
| <span data-ttu-id="efc51-461">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-461">Divorced</span></span>               | <span data-ttu-id="efc51-462">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-462">Divorced</span></span>             |
| <span data-ttu-id="efc51-463">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="efc51-463">Registered Partnership</span></span> | <span data-ttu-id="efc51-464">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="efc51-464">Domestic Partnership</span></span> |
| <span data-ttu-id="efc51-465">None</span><span class="sxs-lookup"><span data-stu-id="efc51-465">None</span></span>                   | <span data-ttu-id="efc51-466">None</span><span class="sxs-lookup"><span data-stu-id="efc51-466">None</span></span>                 |
| <span data-ttu-id="efc51-467">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="efc51-467">Cohabiting</span></span>             | <span data-ttu-id="efc51-468">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="efc51-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="efc51-469">เพศ</span><span class="sxs-lookup"><span data-stu-id="efc51-469">Gender</span></span>

<span data-ttu-id="efc51-470">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="efc51-471">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="efc51-472">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-472">Human Resources</span></span>       | <span data-ttu-id="efc51-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="efc51-474">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="efc51-474">Male</span></span>         | <span data-ttu-id="efc51-475">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="efc51-475">Male</span></span>            |
| <span data-ttu-id="efc51-476">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="efc51-476">Female</span></span>       | <span data-ttu-id="efc51-477">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="efc51-477">Female</span></span>          |
| <span data-ttu-id="efc51-478">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="efc51-478">Non-specific</span></span> | <span data-ttu-id="efc51-479">*ไม่สนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="efc51-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="efc51-480">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-480">Earning codes</span></span>

<span data-ttu-id="efc51-481">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="efc51-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="efc51-482">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="efc51-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="efc51-483">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="efc51-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="efc51-484">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="efc51-484">Supported frequencies</span></span>

- <span data-ttu-id="efc51-485">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="efc51-485">All</span></span>
- <span data-ttu-id="efc51-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="efc51-486">EVERYPAY</span></span>
- <span data-ttu-id="efc51-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="efc51-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="efc51-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="efc51-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="efc51-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="efc51-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="efc51-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-490">1OFMTH</span></span>
- <span data-ttu-id="efc51-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-491">LASTOFMTH</span></span>
- <span data-ttu-id="efc51-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-492">2OFMTH</span></span>
- <span data-ttu-id="efc51-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-493">3OFMTH</span></span>
- <span data-ttu-id="efc51-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-494">4OFMTH</span></span>
- <span data-ttu-id="efc51-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-495">5OFMTH</span></span>
- <span data-ttu-id="efc51-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-496">1N2OFMTH</span></span>
- <span data-ttu-id="efc51-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-497">3N4OFMTH</span></span>
- <span data-ttu-id="efc51-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-498">1N3OFMTH</span></span>
- <span data-ttu-id="efc51-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-499">1N4OFMTH</span></span>
- <span data-ttu-id="efc51-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-500">2N3OFMTH</span></span>
- <span data-ttu-id="efc51-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-501">2N4OFMTH</span></span>
- <span data-ttu-id="efc51-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="efc51-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="efc51-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="efc51-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="efc51-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="efc51-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="efc51-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="efc51-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="efc51-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="efc51-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="efc51-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="efc51-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="efc51-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="efc51-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="efc51-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="efc51-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="efc51-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="efc51-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="efc51-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="efc51-514">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="efc51-514">Addresses</span></span>

<span data-ttu-id="efc51-515">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="efc51-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="efc51-516">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="efc51-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="efc51-517">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-517">Human Resources</span></span>          | <span data-ttu-id="efc51-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="efc51-519">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="efc51-519">Country/Region</span></span>  | <span data-ttu-id="efc51-520">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="efc51-520">Country Code</span></span>          |
| <span data-ttu-id="efc51-521">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="efc51-521">Zip/Postal Code</span></span> | <span data-ttu-id="efc51-522">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="efc51-522">Postal Code</span></span>           |
| <span data-ttu-id="efc51-523">สถานะ</span><span class="sxs-lookup"><span data-stu-id="efc51-523">State</span></span>           | <span data-ttu-id="efc51-524">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="efc51-524">State Code</span></span>            |
| <span data-ttu-id="efc51-525">เมือง</span><span class="sxs-lookup"><span data-stu-id="efc51-525">City</span></span>            | <span data-ttu-id="efc51-526">เมือง</span><span class="sxs-lookup"><span data-stu-id="efc51-526">City</span></span>                  |
| <span data-ttu-id="efc51-527">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="efc51-527">County</span></span>          | <span data-ttu-id="efc51-528">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="efc51-528">County (Municipality)</span></span> |
| <span data-ttu-id="efc51-529">ถนน</span><span class="sxs-lookup"><span data-stu-id="efc51-529">Street</span></span>          | <span data-ttu-id="efc51-530">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="efc51-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="efc51-531">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="efc51-531">Tax regions</span></span>

<span data-ttu-id="efc51-532">ภูมิภาคการเก็บภาษีถูกใช้เพื่อกำหนดภาษีที่เหมาะสมที่ควรนำมาใช้ในระหว่างการสร้างระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="efc51-533">ภูมิภาคการเก็บภาษีถูกแม็ปไปยัง Dayforce เป็นที่อยู่ของสถานที่</span><span class="sxs-lookup"><span data-stu-id="efc51-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="efc51-534">ภูมิภาคการเก็บภาษีเริ่มต้นต้องเชื่อมโยงกับตำแหน่งงานที่ใช้งานอยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="efc51-535">ภูมิภาคการเก็บภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-535">Tax region (required)</span></span>
- <span data-ttu-id="efc51-536">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-536">Country/Region (required)</span></span>
- <span data-ttu-id="efc51-537">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-537">State (required)</span></span>
- <span data-ttu-id="efc51-538">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="efc51-538">County</span></span> 
- <span data-ttu-id="efc51-539">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="efc51-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="efc51-540">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="efc51-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="efc51-541">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในเม็กซิโก ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efc51-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="efc51-542">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-542">Departments are required on positions.</span></span>
- <span data-ttu-id="efc51-543">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="efc51-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="efc51-544">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-544">Job types</span></span>

<span data-ttu-id="efc51-545">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="efc51-546">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="efc51-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="efc51-547">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="efc51-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="efc51-548">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="efc51-549">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="efc51-550">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-550">Job type</span></span>   | <span data-ttu-id="efc51-551">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="efc51-552">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="efc51-552">Hourly</span></span>     | <span data-ttu-id="efc51-553">MX รายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="efc51-553">MX Hourly</span></span>   |
| <span data-ttu-id="efc51-554">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-554">Salaried</span></span>   | <span data-ttu-id="efc51-555">MX รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="efc51-556">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-556">Position types</span></span> 

<span data-ttu-id="efc51-557">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="efc51-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="efc51-558">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="efc51-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="efc51-559">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="efc51-560">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="efc51-560">Position type</span></span>   | <span data-ttu-id="efc51-561">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="efc51-562">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="efc51-562">Full-time</span></span>       | <span data-ttu-id="efc51-563">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="efc51-563">Full time employee</span></span> |
| <span data-ttu-id="efc51-564">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="efc51-564">Part-time</span></span>       | <span data-ttu-id="efc51-565">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="efc51-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="efc51-566">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="efc51-566">Reason codes</span></span>

<span data-ttu-id="efc51-567">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="efc51-568">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="efc51-569">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="efc51-570">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="efc51-570">Reason code</span></span>            | <span data-ttu-id="efc51-571">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-571">Description</span></span>                    | <span data-ttu-id="efc51-572">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="efc51-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="efc51-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="efc51-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="efc51-574">การออกก่อนค่าจ้างแรก</span><span class="sxs-lookup"><span data-stu-id="efc51-574">Departure before first payroll</span></span> | <span data-ttu-id="efc51-575">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-575">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-576">การลาออก</span><span class="sxs-lookup"><span data-stu-id="efc51-576">RESIGNATION</span></span>            | <span data-ttu-id="efc51-577">การลาออก</span><span class="sxs-lookup"><span data-stu-id="efc51-577">Resignation</span></span>                    | <span data-ttu-id="efc51-578">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-578">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-579">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="efc51-579">PENSION</span></span>                | <span data-ttu-id="efc51-580">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="efc51-580">Pension</span></span>                        | <span data-ttu-id="efc51-581">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-581">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-582">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-582">TERMINATION</span></span>            | <span data-ttu-id="efc51-583">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-583">Termination</span></span>                    | <span data-ttu-id="efc51-584">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-584">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-585">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="efc51-585">RETIREMENT</span></span>             | <span data-ttu-id="efc51-586">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="efc51-586">Retirement</span></span>                     | <span data-ttu-id="efc51-587">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-587">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-588">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-588">ABSENTEE</span></span>               | <span data-ttu-id="efc51-589">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-589">Absentee</span></span>                       | <span data-ttu-id="efc51-590">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-590">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-591">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-591">OTHER</span></span>                  | <span data-ttu-id="efc51-592">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-592">Other Reasons</span></span>                  | <span data-ttu-id="efc51-593">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-593">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-594">การปิด</span><span class="sxs-lookup"><span data-stu-id="efc51-594">CLOSURE</span></span>                | <span data-ttu-id="efc51-595">การปิดของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="efc51-595">Business Closure</span></span>               | <span data-ttu-id="efc51-596">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-596">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-597">ความตาย</span><span class="sxs-lookup"><span data-stu-id="efc51-597">DEATH</span></span>                  | <span data-ttu-id="efc51-598">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="efc51-598">Death</span></span>                          | <span data-ttu-id="efc51-599">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-599">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="efc51-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="efc51-601">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="efc51-601">Leave of Absence</span></span>               | <span data-ttu-id="efc51-602">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-602">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="efc51-603">CONTRACTEND</span></span>            | <span data-ttu-id="efc51-604">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="efc51-604">End of Contract</span></span>                | <span data-ttu-id="efc51-605">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-605">Terminate worker</span></span>     |
| <span data-ttu-id="efc51-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="efc51-606">SALARYCHANGE</span></span>           | <span data-ttu-id="efc51-607">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="efc51-607">Change of Salary</span></span>               | <span data-ttu-id="efc51-608">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="efc51-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="efc51-609">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-609">Terms of employment</span></span>

<span data-ttu-id="efc51-610">มีการใช้เงื่อนไขของการจ้างงาน เพื่อสร้างประเภทและตัวอย่างของการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="efc51-611">เงื่อนไขถูกแม็ปกับ Dayforce เป็นค่าตัวบ่งชี้การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="efc51-612">เงื่อนไขการจ้างงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="efc51-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="efc51-613">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-613">Terms of employment</span></span>   | <span data-ttu-id="efc51-614">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="efc51-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="efc51-615">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="efc51-615">Regular</span></span>               | <span data-ttu-id="efc51-616">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="efc51-616">Regular</span></span>     |
| <span data-ttu-id="efc51-617">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="efc51-617">Direct</span></span>                | <span data-ttu-id="efc51-618">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="efc51-618">Direct</span></span>      |
| <span data-ttu-id="efc51-619">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-619">Internship</span></span>            | <span data-ttu-id="efc51-620">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-620">Internship</span></span>  |
| <span data-ttu-id="efc51-621">ถาวร</span><span class="sxs-lookup"><span data-stu-id="efc51-621">Permanent</span></span>             | <span data-ttu-id="efc51-622">ถาวร</span><span class="sxs-lookup"><span data-stu-id="efc51-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="efc51-623">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="efc51-623">Marital status</span></span>

<span data-ttu-id="efc51-624">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="efc51-625">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="efc51-626">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-626">Human Resources</span></span>                 | <span data-ttu-id="efc51-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="efc51-628">สมรส</span><span class="sxs-lookup"><span data-stu-id="efc51-628">Married</span></span>                | <span data-ttu-id="efc51-629">สมรส</span><span class="sxs-lookup"><span data-stu-id="efc51-629">Married</span></span>                   |
| <span data-ttu-id="efc51-630">โสด</span><span class="sxs-lookup"><span data-stu-id="efc51-630">Single</span></span>                 | <span data-ttu-id="efc51-631">โสด</span><span class="sxs-lookup"><span data-stu-id="efc51-631">Single</span></span>                    |
| <span data-ttu-id="efc51-632">หม้าย</span><span class="sxs-lookup"><span data-stu-id="efc51-632">Widowed</span></span>                | <span data-ttu-id="efc51-633">หม้าย</span><span class="sxs-lookup"><span data-stu-id="efc51-633">Widowed</span></span>                   |
| <span data-ttu-id="efc51-634">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-634">Divorced</span></span>               | <span data-ttu-id="efc51-635">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-635">Divorced</span></span>                  |
| <span data-ttu-id="efc51-636">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="efc51-636">Registered Partnership</span></span> | <span data-ttu-id="efc51-637">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="efc51-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="efc51-638">None</span><span class="sxs-lookup"><span data-stu-id="efc51-638">None</span></span>                   | <span data-ttu-id="efc51-639">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="efc51-640">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="efc51-640">Cohabiting</span></span>             | <span data-ttu-id="efc51-641">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="efc51-642">เพศ</span><span class="sxs-lookup"><span data-stu-id="efc51-642">Gender</span></span>

<span data-ttu-id="efc51-643">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="efc51-644">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="efc51-645">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-645">Human Resources</span></span>       | <span data-ttu-id="efc51-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="efc51-647">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="efc51-647">Male</span></span>         | <span data-ttu-id="efc51-648">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="efc51-648">Male</span></span>                      |
| <span data-ttu-id="efc51-649">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="efc51-649">Female</span></span>       | <span data-ttu-id="efc51-650">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="efc51-650">Female</span></span>                    |
| <span data-ttu-id="efc51-651">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="efc51-651">Non-specific</span></span> | <span data-ttu-id="efc51-652">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="efc51-653">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="efc51-653">Payment method</span></span>

<span data-ttu-id="efc51-654">วิธีการชำระเงินให้พนักงานและบริษัทมีวิธีในการอธิบายวิธีการจ่ายเงินแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="efc51-655">วิธีการชำระเงินถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="efc51-656">ตารางต่อไปนี้แสดงวิธีการแม็ปวิธีการชำระเงินกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="efc51-657">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-657">Human Resources</span></span>             | <span data-ttu-id="efc51-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="efc51-659">เงินสด</span><span class="sxs-lookup"><span data-stu-id="efc51-659">Cash</span></span>               | <span data-ttu-id="efc51-660">เงินสด</span><span class="sxs-lookup"><span data-stu-id="efc51-660">Cash</span></span>                      |
| <span data-ttu-id="efc51-661">การชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="efc51-661">Electronic Payment</span></span> | <span data-ttu-id="efc51-662">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="efc51-662">Transfer</span></span>                  |
| <span data-ttu-id="efc51-663">ตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="efc51-663">Check</span></span>              | <span data-ttu-id="efc51-664">เช็ค</span><span class="sxs-lookup"><span data-stu-id="efc51-664">Cheque</span></span>                    |
| <span data-ttu-id="efc51-665">ตั๋วแลกเงินธนาคาร</span><span class="sxs-lookup"><span data-stu-id="efc51-665">Bank Draft</span></span>         | <span data-ttu-id="efc51-666">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="efc51-667">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="efc51-667">Other</span></span>              | <span data-ttu-id="efc51-668">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="efc51-669">ชนิดของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="efc51-669">Bank account type</span></span>

<span data-ttu-id="efc51-670">ชนิดของบัญชีธนาคารถูกใช้สำหรับการชำระเงินทางอิเล็กทรอนิกส์แก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="efc51-671">ชนิดบัญชีธนาคารถูกแม็ปกับ Dayforce เป็นข้อมูลบัญชีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="efc51-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="efc51-672">ชนิดของบัญชีธนาคารจะถูกแปล ตามความเหมาะสม กับค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="efc51-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="efc51-673">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-673">Human Resources</span></span>            | <span data-ttu-id="efc51-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="efc51-675">บัญชีกระแสรายวัน</span><span class="sxs-lookup"><span data-stu-id="efc51-675">Checking Account</span></span>  | <span data-ttu-id="efc51-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="efc51-676">CheckingAccount</span></span>           |
| <span data-ttu-id="efc51-677">บัญชีเครดิตค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="efc51-677">Payroll Account</span></span>   | <span data-ttu-id="efc51-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="efc51-678">PayrollAccount</span></span>            |
| <span data-ttu-id="efc51-679">บัญชีออมทรัพย์</span><span class="sxs-lookup"><span data-stu-id="efc51-679">Savings Account</span></span>   | <span data-ttu-id="efc51-680">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="efc51-681">บัญชี BankGirot</span><span class="sxs-lookup"><span data-stu-id="efc51-681">BankGirot account</span></span> | <span data-ttu-id="efc51-682">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="efc51-683">บัญชี PlusGirot</span><span class="sxs-lookup"><span data-stu-id="efc51-683">PlusGirot account</span></span> | <span data-ttu-id="efc51-684">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="efc51-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="efc51-685">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="efc51-685">Earning codes</span></span>

<span data-ttu-id="efc51-686">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="efc51-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="efc51-687">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="efc51-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="efc51-688">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="efc51-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="efc51-689">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="efc51-689">Supported frequencies</span></span>

- <span data-ttu-id="efc51-690">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="efc51-690">All</span></span>
- <span data-ttu-id="efc51-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="efc51-691">EVERYPAY</span></span>
- <span data-ttu-id="efc51-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="efc51-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="efc51-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="efc51-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="efc51-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="efc51-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="efc51-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-695">1OFMTH</span></span>
- <span data-ttu-id="efc51-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-696">LASTOFMTH</span></span>
- <span data-ttu-id="efc51-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-697">2OFMTH</span></span>
- <span data-ttu-id="efc51-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-698">3OFMTH</span></span>
- <span data-ttu-id="efc51-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-699">4OFMTH</span></span>
- <span data-ttu-id="efc51-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-700">5OFMTH</span></span>
- <span data-ttu-id="efc51-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-701">1N2OFMTH</span></span>
- <span data-ttu-id="efc51-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-702">3N4OFMTH</span></span>
- <span data-ttu-id="efc51-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-703">1N3OFMTH</span></span>
- <span data-ttu-id="efc51-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-704">1N4OFMTH</span></span>
- <span data-ttu-id="efc51-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-705">2N3OFMTH</span></span>
- <span data-ttu-id="efc51-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-706">2N4OFMTH</span></span>
- <span data-ttu-id="efc51-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="efc51-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="efc51-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="efc51-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="efc51-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="efc51-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="efc51-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="efc51-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="efc51-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="efc51-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="efc51-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="efc51-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="efc51-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="efc51-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="efc51-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="efc51-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="efc51-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="efc51-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="efc51-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="efc51-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="efc51-719">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="efc51-719">Addresses</span></span>

<span data-ttu-id="efc51-720">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="efc51-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="efc51-721">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="efc51-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="efc51-722">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="efc51-722">Human Resources</span></span>              | <span data-ttu-id="efc51-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="efc51-724">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="efc51-724">Country/Region</span></span>      | <span data-ttu-id="efc51-725">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="efc51-725">Country Code</span></span>          |
| <span data-ttu-id="efc51-726">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="efc51-726">Zip/Postal Code</span></span>     | <span data-ttu-id="efc51-727">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="efc51-727">Postal Code</span></span>           |
| <span data-ttu-id="efc51-728">สถานะ</span><span class="sxs-lookup"><span data-stu-id="efc51-728">State</span></span>               | <span data-ttu-id="efc51-729">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="efc51-729">State Code</span></span>            |
| <span data-ttu-id="efc51-730">เมือง</span><span class="sxs-lookup"><span data-stu-id="efc51-730">City</span></span>                | <span data-ttu-id="efc51-731">เมือง</span><span class="sxs-lookup"><span data-stu-id="efc51-731">City</span></span>                  |
| <span data-ttu-id="efc51-732">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="efc51-732">County</span></span>              | <span data-ttu-id="efc51-733">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="efc51-733">County (Municipality)</span></span> |
| <span data-ttu-id="efc51-734">ถนน</span><span class="sxs-lookup"><span data-stu-id="efc51-734">Street</span></span>              | <span data-ttu-id="efc51-735">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="efc51-735">Address Line 1</span></span>        |
| <span data-ttu-id="efc51-736">หมายเลขถนน</span><span class="sxs-lookup"><span data-stu-id="efc51-736">Street Number</span></span>       | <span data-ttu-id="efc51-737">ที่อยู่ บรรทัดที่ 2</span><span class="sxs-lookup"><span data-stu-id="efc51-737">Address Line 2</span></span>        |
| <span data-ttu-id="efc51-738">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="efc51-738">Building Complement</span></span> | <span data-ttu-id="efc51-739">ที่อยู่ บรรทัดที่ 5</span><span class="sxs-lookup"><span data-stu-id="efc51-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="efc51-740">หมายเลขหนังสือเดินทาง</span><span class="sxs-lookup"><span data-stu-id="efc51-740">Passport number</span></span>

<span data-ttu-id="efc51-741">พนักงานสามารถประกาศข้อมูลหนังสือเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="efc51-741">Employees can declare passport information.</span></span> <span data-ttu-id="efc51-742">ข้อมูลนี้เป็นชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง** และถูกรวมอยู่ใน Dayforce เป็นส่วนหนึ่งของข้อมูลเม็กซิโกเฉพาะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="efc51-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="efc51-743">ชนิดการระบุรหัสประจำตัว = "หนังสือเดินทาง"</span><span class="sxs-lookup"><span data-stu-id="efc51-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="efc51-744">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="efc51-744">Issued Date</span></span>
- <span data-ttu-id="efc51-745">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="efc51-745">Expiration Date</span></span>

<span data-ttu-id="efc51-746">พนักงานสามารถประกาศหมายเลขรหัสหลายเลขของชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="efc51-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="efc51-747">อย่างไรก็ตาม เฉพาะรายการหนังสือเดินทางที่ใช้งานปัจจุบันจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="efc51-748">ถ้ารายการหนังสือเดินทางทั้งหมดหมดอายุ หนังสือเดินทางที่ออกครั้งล่าสุดจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="efc51-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]