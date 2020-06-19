---
title: ตั้งค่าคอนฟิกการรวมกับ Dayforce
description: การรวมระหว่าง Microsoft Dynamics 365 Human Resources และ Ceridian Dayforce ขึ้นอยู่กับขั้นตอนการตั้งค่าคอนฟิกหลายขั้นตอนที่อธิบายไว้ในบทความนี้ คุณต้องตั้งค่าคอนฟิกการรวมทั้งในทรัพยากรบุคคลและ Dayforce ก่อนที่คุณจะสามารถประมวลผลรันการจ่ายเงิน
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: c66ec772ea66732e042f50081f04a6569852f211
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431302"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="087b0-104">ตั้งค่าคอนฟิกการรวมกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="087b0-105">การรวมระหว่าง Microsoft Dynamics 365 Human Resources และ Ceridian Dayforce ขึ้นอยู่กับขั้นตอนการตั้งค่าคอนฟิกหลายขั้นตอนที่อธิบายไว้ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="087b0-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="087b0-106">คุณต้องตั้งค่าคอนฟิกการรวมทั้งในทรัพยากรบุคคลและ Dayforce ก่อนที่คุณจะสามารถประมวลผลรันการจ่ายเงิน</span><span class="sxs-lookup"><span data-stu-id="087b0-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="087b0-107">เมื่อคุณใช้บริการ เช่น Dayforce เพื่อทำให้รันการจ่ายเงินให้เสร็จสมบูรณ์ คุณต้องเปิดใช้งานการรวมในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="087b0-108">การรวมจำเป็นต้องมีข้อมูลที่เฉพาะเจาะจงจากทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="087b0-109">ดังนั้น คุณต้องตรวจสอบว่าข้อมูลที่มีการแม็ปกับ Dayforce ถูกตั้งค่าคอนฟิกในทรัพยากรบุคคลในลักษณะที่สนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="087b0-110">การรวมใช้ประเภทที่กว้างของข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="087b0-111">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-111">Human resources data</span></span>
- <span data-ttu-id="087b0-112">ข้อมูลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-112">Compensation data</span></span>
- <span data-ttu-id="087b0-113">ข้อมูลค่าจ้าง เช่น รอบการชำระค่าจ้าง รอบระยะเวลาการชำระค่าจ้าง และรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="087b0-114">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-114">Worker data</span></span>

<span data-ttu-id="087b0-115">บทความนี้อธิบายขั้นตอนต่างๆ ที่คุณต้องปฏิบัติตามเพื่อเปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="087b0-116">นอกจากนี้ ยังอธิบายถึงชนิดของข้อมูลและรายละเอียดการตั้งค่าคอนฟิกที่การรวมต้องการ</span><span class="sxs-lookup"><span data-stu-id="087b0-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="087b0-117">เปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-117">Enable the integration</span></span>

<span data-ttu-id="087b0-118">ในทรัพยากรบุคคล คุณต้องเปิดใช้งานการรวมและป้อนข้อมูลการตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="087b0-119">ถ้าคุณต้องการธุรกรรมบัญชีแยกประเภททั่วไปที่ถูกผลิตให้ถูกนำเข้าลงใน Microsoft Dynamics 365 Finance คุณยังต้องตั้งค่าบัญชีที่จัดเก็บ Microsoft Azure และป้อนสตริงการเชื่อมต่อที่จัดเก็บ Azure ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="087b0-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="087b0-120">เมื่อต้องการเปิดใช้งานการรวมในในทรัพยากรบุคคล ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="087b0-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="087b0-121">ในหน้า **การดูแลระบบ** เลือก **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="087b0-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="087b0-122">ป้อนปลายทาง File Transfer Protocol (FTP) แบบปลอดภัย และพาธโฟลเดอร์ FTP แบบปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="087b0-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="087b0-123">ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่จะเข้าถึงปลายทาง FTP แบบปลอดภัย และโฟลเดอร์พาธ</span><span class="sxs-lookup"><span data-stu-id="087b0-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="087b0-124">ทดสอบการเชื่อมต่อ หากจำเป็น และตั้งค่าตัวเลือก **เปิดใช้งานการรวมค่าจ้าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="087b0-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="087b0-125">เมื่อเปิดการรวม มีการสร้างแพคเกจการส่งออกข้อมูลและไฟล์ และมีการตั้งค่าความถี่</span><span class="sxs-lookup"><span data-stu-id="087b0-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="087b0-126">คุณสามารถเปลี่ยนความถี่นี้ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="087b0-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="087b0-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบัญชีการจัดเก็บ Azure และสตริงการเชื่อมต่อการจัดเก็บ Azure ให้ดูบทความ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="087b0-128">เกี่ยวกับบัญชีการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="087b0-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="087b0-129">ตั้งค่าคอนฟิกสตริงการเชื่อมต่อการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="087b0-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="087b0-130">รายละเอียดทางเทคนิค เมื่อเปิดใช้งานการรวมค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="087b0-131">การเปิดการรวมค่าจ้างมีผลกระทบหลักสองประการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="087b0-132">โครงการส่งออกข้อมูลที่มีชื่อว่า "การส่งออกการรวมค่าจ้าง" ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="087b0-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="087b0-133">โครงการนี้ประกอบด้วยเอนทิตีและฟิลด์ที่จำเป็นสำหรับการรวมค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="087b0-134">เมื่อต้องการตรวจสอบโครงการ ให้ไปที่ **การจัดการระบบ** เลือกไทล์ **การจัดการข้อมูล** แล้วเปิดโครงการข้อมูลจากรายการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="087b0-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="087b0-135">ชุดงานนี้จะดำเนินการโครงการส่งออกข้อมูล เข้ารหัสแพคเกจข้อมูลที่เป็นผลลัพธ์ และโอนย้ายไฟล์แพคเกจข้อมูลไปยังปลายทาง SFTP ที่ตั้งค่าคอนฟิกบนหน้าจอ **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="087b0-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="087b0-136">แพคเกจข้อมูลที่โอนย้ายไปยังปลายทาง SFTP ถูกเข้ารหัสโดยใช้คีย์ที่ไม่ซ้ำกันสำหรับแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="087b0-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="087b0-137">คีย์อยู่ใน Azure Key Vault ที่สามารถเข้าถึงได้โดย Ceridian เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="087b0-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="087b0-138">ไม่สามารถถอดรหัสและตรวจสอบเนื้อหาของแพคเกจข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="087b0-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="087b0-139">ถ้าคุณต้องการตรวจสอบเนื้อหาของแพคเกจข้อมูล คุณต้องส่งออกโครงการข้อมูล "การส่งออกการรวมบัญชีค่าจ้าง" ด้วยตนเอง ให้ดาวน์โหลดโครงการนั้น แล้วเปิด</span><span class="sxs-lookup"><span data-stu-id="087b0-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="087b0-140">การส่งออกด้วยตนเองจะไม่ใช้การเข้ารหัสหรือโอนย้ายบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="087b0-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="087b0-141">ตั้งค่าคอนฟิกข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="087b0-141">Configure your data</span></span> 

<span data-ttu-id="087b0-142">ในการประมวลผลค่าจ้าง คุณต้องตั้งค่าคอนฟิกข้อมูลทรัพยากรบุคคลในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="087b0-143">คุณต้องตั้งค่าข้อมูลองค์กร เช่น งาน และตำแหน่ง พร้อมด้วยข้อมูลค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="087b0-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="087b0-144">ข้อมูลนี้ให้ข้อมูลการจ้างงาน ค่าจ้าง และการหักลด ที่จำเป็นในการสร้างค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="087b0-145">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="087b0-146">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="087b0-146">Benefits</span></span> 

<span data-ttu-id="087b0-147">ทรัพยากรบุคคลให้เครื่องมือสำหรับการตั้งค่าและการบำรุงรักษาของสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงาน ที่หน่วยงานนำเสนอหรือประมวลผลสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="087b0-148">เมื่อคุณสร้างสวัสดิการ พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="087b0-149">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="087b0-149">Benefit plans</span></span>

- <span data-ttu-id="087b0-150">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-150">Plan (required)</span></span>
- <span data-ttu-id="087b0-151">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-151">Type (required)</span></span>
- <span data-ttu-id="087b0-152">ผลกระทบของค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-152">Payroll impact (required)</span></span>
- <span data-ttu-id="087b0-153">ขอคืนเงินค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="087b0-153">Recover arrears</span></span>
- <span data-ttu-id="087b0-154">วิธีการหักลด</span><span class="sxs-lookup"><span data-stu-id="087b0-154">Deduction method</span></span>
- <span data-ttu-id="087b0-155">ระดับความสำคัญการหักลด</span><span class="sxs-lookup"><span data-stu-id="087b0-155">Deduction priority</span></span>
- <span data-ttu-id="087b0-156">จำกัดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="087b0-156">Limit period</span></span>
- <span data-ttu-id="087b0-157">ยอดวงเงิน</span><span class="sxs-lookup"><span data-stu-id="087b0-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="087b0-158">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="087b0-158">Benefits</span></span>

- <span data-ttu-id="087b0-159">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-159">Plan (required)</span></span>
- <span data-ttu-id="087b0-160">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-160">Type (required)</span></span>
- <span data-ttu-id="087b0-161">ตัวเลือก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-161">Option (required)</span></span>
- <span data-ttu-id="087b0-162">รหัสสวัสดิการ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-162">Benefit ID (required)</span></span>
- <span data-ttu-id="087b0-163">ความถี่</span><span class="sxs-lookup"><span data-stu-id="087b0-163">Frequency</span></span>
- <span data-ttu-id="087b0-164">ข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="087b0-164">Basis</span></span>
- <span data-ttu-id="087b0-165">ยอดเงินหรืออัตรา</span><span class="sxs-lookup"><span data-stu-id="087b0-165">Amount or rate</span></span>
- <span data-ttu-id="087b0-166">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="087b0-167">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="087b0-167">Supported frequencies</span></span> 

- <span data-ttu-id="087b0-168">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="087b0-168">Weekly</span></span>
- <span data-ttu-id="087b0-169">ทุกสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="087b0-169">Bi-weekly</span></span>
- <span data-ttu-id="087b0-170">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-170">Semi-monthly</span></span>
- <span data-ttu-id="087b0-171">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="087b0-172">ฐานที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="087b0-172">Supported bases</span></span> 

- <span data-ttu-id="087b0-173">ยอดเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="087b0-173">Fixed amount</span></span>
- <span data-ttu-id="087b0-174">เปอร์เซ็นต์ของรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-174">Percent of earnings</span></span>
- <span data-ttu-id="087b0-175">ชั่วโมงที่มีประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-175">Productive hours</span></span>

<span data-ttu-id="087b0-176">Dayforce สร้างการหักลดต่อไปนี้ โดยขึ้นอยู่กับผลกระทบของค่าจ้างที่กำหนดในแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="087b0-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="087b0-177">การเลือกในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-177">Selection in Human Resources</span></span>        | <span data-ttu-id="087b0-178">ผลลัพธ์ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="087b0-179">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="087b0-179">None</span></span>                       | <span data-ttu-id="087b0-180">ไม่มีการสร้างการหักลด</span><span class="sxs-lookup"><span data-stu-id="087b0-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="087b0-181">การหักลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="087b0-181">Deduction only</span></span>             | <span data-ttu-id="087b0-182">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="087b0-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="087b0-183">การจ่ายเงินสมทบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="087b0-183">Contribution only</span></span>          | <span data-ttu-id="087b0-184">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="087b0-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="087b0-185">การหักลดและการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="087b0-185">Deduction and contribution</span></span> | <span data-ttu-id="087b0-186">การหักลดพนักงานและนายจ้างจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="087b0-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="087b0-187">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดและจัดการโปรแกรมสวัสดิการ ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="087b0-188">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="087b0-189">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="087b0-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="087b0-190">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="087b0-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="087b0-191">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="087b0-192">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-192">Compensation</span></span> 

<span data-ttu-id="087b0-193">การจัดการค่าตอบแทนจะใช้ควบคุมการจัดส่งของค่าจ้างพื้นฐานและเงินรางวัล</span><span class="sxs-lookup"><span data-stu-id="087b0-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="087b0-194">ค่าจ้างพื้นฐานคงที่ของพนักงานและการขึ้นค่าตอบแทนตามผลงานจะถูกควบคุมโดยใช้แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="087b0-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="087b0-195">ค่าจ้างจูงใจเช่นการชำระเงินโบนัส รางวัลตามผลการปฏิบัติงาน สิทธิในการซื้อหุ้น การให้หุ้น รางวัลที่จ่ายครั้งเดียว โดยใช้แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="087b0-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="087b0-196">Dayforce ใช้ข้อมูลค่าตอบแทนที่คำนวณอัตรารายชั่วโมงหรือรายปีของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="087b0-197">จำเป็นต้องมีแผนค่าตอบแทนคงที่และการแปลงอัตราค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="087b0-198">พนักงานต้องเชื่อมโยงกับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="087b0-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="087b0-199">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแผนค่าตอบแทน โปรดดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="087b0-200">สร้างแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="087b0-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="087b0-201">สร้างแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="087b0-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="087b0-202">พัฒนาโครงสร้างและแผนเงินเดือน/ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="087b0-203">ประมวลผลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="087b0-204">กำหนดกระบวนการของค่าตอบแทนและคำนวณผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="087b0-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="087b0-205">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="087b0-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="087b0-206">การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="087b0-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="087b0-207">งาน</span><span class="sxs-lookup"><span data-stu-id="087b0-207">Jobs</span></span> 

<span data-ttu-id="087b0-208">งานเป็นชุดของงานและความรับผิดชอบที่ถูกระบุของบุคคลที่ดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="087b0-209">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="087b0-210">การตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="087b0-211">กำหนดงานใหม่</span><span class="sxs-lookup"><span data-stu-id="087b0-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="087b0-212">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-212">Positions</span></span>

<span data-ttu-id="087b0-213">ตำแหน่งคือแต่ละอินสแตนซ์ของงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="087b0-214">ตัวอย่างเช่น ตำแหน่ง "ผู้จัดการฝ่ายขาย (ตะวันออก)" เป็นหนึ่งในตำแหน่งที่เชื่อมโยงกับงาน "ผู้จัดการฝ่ายขาย"</span><span class="sxs-lookup"><span data-stu-id="087b0-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="087b0-215">ตำแหน่งมีอยู่ในแผนก</span><span class="sxs-lookup"><span data-stu-id="087b0-215">A position exists in a department.</span></span> <span data-ttu-id="087b0-216">สามารถเชื่อมโยงผู้ปฏิบัติงานหนึ่งรายกับแต่ละตำแหน่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="087b0-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="087b0-217">เก็บข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ไว้ เมื่อคุณตั้งค่าตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="087b0-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="087b0-218">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-218">Position (required)</span></span>
- <span data-ttu-id="087b0-219">คำอธิบาย (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-219">Description (required)</span></span>
- <span data-ttu-id="087b0-220">งาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-220">Job (required)</span></span>
- <span data-ttu-id="087b0-221">แผนก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-221">Department (required)</span></span>
- <span data-ttu-id="087b0-222">ชนิดตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-222">Position type (required)</span></span>
- <span data-ttu-id="087b0-223">จำนวนบุคลากรเทียบเท่าเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="087b0-223">Full-time equivalent</span></span>
- <span data-ttu-id="087b0-224">ชั่วโมงปกติรายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="087b0-225">ชำระโดยนิติบุคคล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="087b0-226">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-226">Pay cycle (required)</span></span>
- <span data-ttu-id="087b0-227">มิติทางการเงินเริ่มต้น – ศูนย์ต้นทุน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="087b0-228">การมอบหมายผู้ปฏิบัติงาน – ผู้ปฏิบัติงาน การเริ่มต้นการกำหนด การสิ้นสุดการกำหนด รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="087b0-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="087b0-229">ถ้าตำแหน่งหลายตำแหน่งในแผนกเดียวกันเกี่ยวข้องกับงานเดียวกัน จะมีการรวมลงในตำแหน่งหนึ่งๆ ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="087b0-230">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="087b0-231">จัดระเบียบบุคลากรของคุณโดยใช้แผนก งาน และตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="087b0-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="087b0-232">ตั้งค่าตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="087b0-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="087b0-233">แผนก</span><span class="sxs-lookup"><span data-stu-id="087b0-233">Departments</span></span>

<span data-ttu-id="087b0-234">แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="087b0-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="087b0-235">แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="087b0-236">คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="087b0-237">แผนกอาจมีความรับผิดชอบกำไรและขาดทุน</span><span class="sxs-lookup"><span data-stu-id="087b0-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="087b0-238">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="087b0-239">สร้างแผนกและการเชื่อมโยงกับลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="087b0-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="087b0-240">กำหนดฝ่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="087b0-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="087b0-241">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="087b0-242">รอบการชำระค่าจ้างกำหนดความถี่ในการรันค่าจ้าง และจำนวนวันที่เจาะจงเมื่อผู้ปฏิบัติงานได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="087b0-243">ตัวอย่างเช่น รอบการชำระค่าจ้างอาจเป็นรายเดือน และพนักงานอาจได้รับค่าจ้างในวันสุดท้ายของเดือนนั้น</span><span class="sxs-lookup"><span data-stu-id="087b0-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="087b0-244">อีกทางหนึ่งคือ รอบการชำระค่าจ้างอาจเป็นรายสัปดาห์ และพนักงานอาจได้รับค่าจ้างในวันอังคารหลังจากจุดสิ้นสุดของรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="087b0-245">รอบการชำระค่าจ้างถูกกำหนดให้กับตำแหน่ง เพื่อควบคุมเวลาที่ผู้ปฏิบัติงานในตำแหน่งเหล่านั้นได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="087b0-246">หลังจากที่คุณสร้างรอบการชำระค่าจ้าง คุณสามารถสร้างรอบระยะเวลาการชำระค่าจ้างสำหรับแต่ละรอบได้</span><span class="sxs-lookup"><span data-stu-id="087b0-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="087b0-247">รอบการชำระค่าจ้างแต่ละรอบรวมถึงวันที่ของการชำระเงินเริ่มต้นที่ยึดตามข้อมูลที่คุณให้</span><span class="sxs-lookup"><span data-stu-id="087b0-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="087b0-248">อย่างไรก็ตาม คุณสามารถแก้ไขวันที่การชำระเงินเริ่มต้นได้ในรอบการชำระค่าจ้างเพื่อให้อนุญาตการยกเว้น เช่น เมื่อวันที่ชำระเงินตรงกับวันหยุด</span><span class="sxs-lookup"><span data-stu-id="087b0-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="087b0-249">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="087b0-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="087b0-250">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-250">Pay cycle (required)</span></span>
- <span data-ttu-id="087b0-251">ความถี่ของรอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="087b0-252">วันที่เริ่มรอบระยะเวลา (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="087b0-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="087b0-253">วันที่การชำระเงินเริ่มต้น (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="087b0-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="087b0-254">ข้อมูลนี้ถูกรวมเข้ากับ Dayforce เป็นกลุ่มค่าจ้าง และจะถูกแยกตามประเทศหรือภูมิภาคสำหรับรอบการชำระค่าจ้างแต่ละรอบ</span><span class="sxs-lookup"><span data-stu-id="087b0-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="087b0-255">ต้องมีการสร้างรอบระยะเวลาการชำระค่าจ้างอย่างน้อยหนึ่งรายการ ก่อนที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="087b0-256">Dayforce สร้างปฏิทินกลุ่มค่าจ้างและวันที่ในการชำระเงิน โดยยึดตามวันที่เริ่มต้นของรอบระยะเวลาการชำระค่าจ้างแรก และวันที่ชำระเงินเริ่มต้นที่ตั้งค่าในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="087b0-257">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-257">Earning codes</span></span>

<span data-ttu-id="087b0-258">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="087b0-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="087b0-259">รหัสมีพารามิเตอร์ต่าง ๆ ที่เกี่ยวข้องกับรายได้ เช่น แต่ละ กฎทางบัญชี กฎภาษี และรายงานความต้องการและความสามารถในการรวมได้</span><span class="sxs-lookup"><span data-stu-id="087b0-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="087b0-260">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="087b0-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="087b0-261">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-261">Earning Code (required)</span></span>
- <span data-ttu-id="087b0-262">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-262">Description</span></span>
- <span data-ttu-id="087b0-263">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="087b0-263">Unit of measure</span></span>
- <span data-ttu-id="087b0-264">ประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="087b0-265">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-265">Worker data</span></span>

<span data-ttu-id="087b0-266">เรกคอร์ดสำหรับชนิดต่างๆ ของผู้ปฏิบัติงานที่คุณมี มีความสำคัญสำหรับระบบค่าจ้างและทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="087b0-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="087b0-267">ข้อมูลที่คุณป้อนสามารถใช้ติดตามผู้ปฏิบัติงานและข้อมูลส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="087b0-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="087b0-268">คุณสามารถรักษาข้อมูลต่อไปนี้สำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="087b0-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="087b0-269">**พื้นฐาน** – รักษาข้อมูลพื้นฐานเกี่ยวกับผู้ปฏิบัติงาน เช่น ข้อมูลการติดต่อ ข้อมูลทางประชากรศาสตร์ ข้อมูลการระบุรหัสประจำตัว ข้อมูลครอบครัว สถานะการรับราชการทหาร ข้อมูลคนต่างด้าว และผู้ติดต่อได้ในกรณีฉุกเฉินและส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="087b0-270">**การจ้างงาน** – รักษาข้อมูลเกี่ยวกับการจ้างงานของผู้ปฏิบัติงาน เช่น บริษัท หรือสังกัดองค์กร การมอบหมายตำแหน่งงาน วันที่เริ่มต้นและสิ้นสุด สิทธิการทำงาน เงื่อนไขในการจ้างงาน เงินบำนาญ วันหยุดพักผ่อน และข้อมูลการย้ายสถานที่</span><span class="sxs-lookup"><span data-stu-id="087b0-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="087b0-271">**การลางานและการขาดงาน** – รักษาข้อมูลเกี่ยวกับการขาดงานของผู้ปฏิบัติงาน เช่น ปฏิทินการทำงาน ธุรกรรมการขาดงาน และการตั้งค่าการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="087b0-272">**ค่าตอบแทนและค่าจ้าง** – รักษาข้อมูลเกี่ยวกับแผนค่าตอบแทนของผู้ปฏิบัติงานและข้อมูลค่าจ้าง เช่น การลงทะเบียนสำหรับแผน รางวัล ประสิทธิภาพ ค่าคอมมิชชัน ข้อมูลภาษี การเกษียณอายุ และการหักเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="087b0-273">เมื่อคุณป้อนข้อมูลผู้ปฏิบัติงาน พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="087b0-274">ข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="087b0-274">General information</span></span>

- <span data-ttu-id="087b0-275">หมายเลขบุคลากร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-275">Personnel number (required)</span></span>
- <span data-ttu-id="087b0-276">ชื่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-276">First name (required)</span></span>
- <span data-ttu-id="087b0-277">นามสกุล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-277">Last name (required)</span></span>
- <span data-ttu-id="087b0-278">ชื่อกลาง</span><span class="sxs-lookup"><span data-stu-id="087b0-278">Middle name</span></span>
- <span data-ttu-id="087b0-279">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-279">Seniority date</span></span>
- <span data-ttu-id="087b0-280">เรียกว่า</span><span class="sxs-lookup"><span data-stu-id="087b0-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="087b0-281">ข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-281">Personal information</span></span>

- <span data-ttu-id="087b0-282">สถานภาพการสมรส (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-282">Marital status (required)</span></span>
- <span data-ttu-id="087b0-283">วันที่เกิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-283">Birth date (required)</span></span>
- <span data-ttu-id="087b0-284">เพศ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-284">Gender (required)</span></span>
- <span data-ttu-id="087b0-285">บุคคลทุพพลภาพ</span><span class="sxs-lookup"><span data-stu-id="087b0-285">Person with disabilities</span></span>
- <span data-ttu-id="087b0-286">สัญชาติประเทศภูมิภาค (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="087b0-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="087b0-287">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="087b0-287">Address information</span></span>

- <span data-ttu-id="087b0-288">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-288">Primary (required)</span></span>
- <span data-ttu-id="087b0-289">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-289">Country/region (required)</span></span>
- <span data-ttu-id="087b0-290">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-290">Postal code (required)</span></span>
- <span data-ttu-id="087b0-291">หมายเลขถนน (จำเป็น) (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="087b0-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="087b0-292">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="087b0-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="087b0-293">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-293">City (required)</span></span>
- <span data-ttu-id="087b0-294">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-294">State (required)</span></span>
- <span data-ttu-id="087b0-295">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="087b0-296">ข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="087b0-296">Contact information</span></span> 

- <span data-ttu-id="087b0-297">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-297">Primary (required)</span></span>
- <span data-ttu-id="087b0-298">หมายเลขผู้ติดต่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-298">Contact number (required)</span></span>
- <span data-ttu-id="087b0-299">การขยาย</span><span class="sxs-lookup"><span data-stu-id="087b0-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="087b0-300">ข้อมูลค่าจ้างและรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-300">Payroll information and earning codes</span></span>

<span data-ttu-id="087b0-301">พนักงานอาจถูกกำหนดรายได้เฉพาะที่ความถี่ที่กำหนดของการชำระเงิน และมีวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="087b0-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="087b0-302">ฟิลด์ต่อไปนี้จะใช้ใน Dayforce เพื่อช่วยในการรับประกันว่า การกำหนดลักษณะและการตั้งค่าเหล่านั้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="087b0-303">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-303">Earning codes</span></span>

- <span data-ttu-id="087b0-304">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-304">Position (required)</span></span>
- <span data-ttu-id="087b0-305">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-305">Earning Code (required)</span></span>
- <span data-ttu-id="087b0-306">ความถี่ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-306">Frequency (required)</span></span>
- <span data-ttu-id="087b0-307">จำนวน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="087b0-308">ข้อมูลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-308">Payroll information</span></span>

- <span data-ttu-id="087b0-309">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="087b0-309">Payment Method</span></span>
- <span data-ttu-id="087b0-310">ภูมิภาคเศรษฐกิจ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-310">Economic Region (required)</span></span>
- <span data-ttu-id="087b0-311">รหัสสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-311">Employee Benefits ID</span></span>
- <span data-ttu-id="087b0-312">หมายเลขรหัสประจำชาติ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-312">National ID Number (required)</span></span>
- <span data-ttu-id="087b0-313">หมายเลขการรับราชการทหาร</span><span class="sxs-lookup"><span data-stu-id="087b0-313">Military Service Number</span></span>
- <span data-ttu-id="087b0-314">รหัสกะ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-314">Shift ID (required)</span></span>
- <span data-ttu-id="087b0-315">หมายเลขภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-315">Tax Number (required)</span></span>
- <span data-ttu-id="087b0-316">รหัสสหภาพ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-316">Union ID (required)</span></span>
- <span data-ttu-id="087b0-317">รหัสวันทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-317">Work Day ID (required)</span></span>
- <span data-ttu-id="087b0-318">หมายเลขใบอนุญาตทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="087b0-319">สำหรับวิธีการชำระเงิน เม็กซิโกสนับสนุน **เงินสด** **เช็ค** (เช็คจริงของบริษัท) และ **การชำระเงินทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="087b0-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="087b0-320">ถ้าไม่มีการระบุวิธีการชำระเงิน **เช็ค** จะถูกใช้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="087b0-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="087b0-321">รายละเอียดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-321">Employment details</span></span>

<span data-ttu-id="087b0-322">ประวัติรายละเอียดตการจ้างงานถูกใช้เป็นข้อมูลสำคัญในการสืบทอดการพนักงานจ้างงานของพนักงาน การหยุดชะงัก และสถานะการจ้างงานใหม่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="087b0-323">Dayforce สนับสนุนเรกคอร์ดการจ้างงานที่ใช้งานอยู่เพียงรายการเดียวในแต่ละครั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="087b0-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="087b0-324">วันที่เริ่มต้นการจ้างงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-324">Employment start date (required)</span></span>
- <span data-ttu-id="087b0-325">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-325">Employment end date</span></span>
- <span data-ttu-id="087b0-326">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="087b0-326">Start date</span></span>
- <span data-ttu-id="087b0-327">วันที่เริ่มต้นที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="087b0-327">Adjusted start date</span></span>
- <span data-ttu-id="087b0-328">วันที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="087b0-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="087b0-329">เหตุผลที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="087b0-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="087b0-330">วันสำคัญของพนักงานได้รับมาโดยใช้ข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="087b0-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="087b0-331">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-331">Human Resources</span></span>                | <span data-ttu-id="087b0-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="087b0-333">วันที่จ้างงานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="087b0-333">Most recent hire date</span></span> | <span data-ttu-id="087b0-334">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="087b0-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="087b0-335">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-335">Termination date</span></span>      | <span data-ttu-id="087b0-336">วันที่สิ้นสุดการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="087b0-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="087b0-337">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="087b0-337">Start date</span></span>            | <span data-ttu-id="087b0-338">วันที่เริ่มต้นที่ปรับปรุงแล้ว วันที่เริ่มต้น หรือการเริ่มต้นการจ้างงานของเรกคอร์ประวัติการจ้างงานที่ไม่ได้ใช้งานอยู่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="087b0-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="087b0-339">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="087b0-339">Original hire date</span></span>    | <span data-ttu-id="087b0-340">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานแรกสุด</span><span class="sxs-lookup"><span data-stu-id="087b0-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="087b0-341">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-341">Compensation</span></span>

<span data-ttu-id="087b0-342">แผนค่าตอบแทนคงต้องเชื่อมโยงกับตำแหน่งหลักของพนักงานทุกตำแหน่ง ตลอดรอบระยะเวลาการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="087b0-343">รอบระยะเวลานี้เริ่มต้นในวันที่ที่พนักงานถูกจ้างงาน (หรือวันที่เริ่มต้นการจ้างงาน) และดำเนินต่อไปจนกว่าจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="087b0-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="087b0-344">วันที่มีผลบังคับใช้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-344">Effective Date (required)</span></span>
- <span data-ttu-id="087b0-345">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="087b0-345">Expiration date</span></span>
- <span data-ttu-id="087b0-346">อัตราการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-346">Pay Rate (required)</span></span>
- <span data-ttu-id="087b0-347">การแปลงอัตราค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="087b0-348">จำนวนเทียบเท่ารายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="087b0-349">จำนวนเทียบเท่ารายชั่วโมง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="087b0-350">ถ้าพนักงานรายชั่วโมงมีตำแหน่งหลายตำแหน่ง ค่าตอบแทนคงที่ของตำแหน่งหลักจะถูกนำเข้าใน Dayforce เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="087b0-351">สำหรับตำแหน่งที่ไม่ใช่ตำแหน่งหลัก อัตรารายชั่วโมงถูกบันทึกลงในตำแหน่งที่สอดคล้องกันใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="087b0-352">ถ้าพนักงานประจำมีตำแหน่งหลายตำแหน่ง จะได้รับอัตราชั่วโมงสะสมและเงินเดือนต่อปีระหว่างตำแหน่งที่ใช้งานอยู่ทั้งหมด และถูกใช้เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="087b0-353">หมายเลขรหัส</span><span class="sxs-lookup"><span data-stu-id="087b0-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="087b0-354">ตัวระบุประกันสังคม</span><span class="sxs-lookup"><span data-stu-id="087b0-354">Social Security identifier</span></span> 

<span data-ttu-id="087b0-355">พนักงานทุกคนต้องมีตัวระบุหลักหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="087b0-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="087b0-356">ตัวระบุนี้ต้องเป็นชนิดรหัส **SSN**</span><span class="sxs-lookup"><span data-stu-id="087b0-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="087b0-357">ใน Dayforce จะได้รับมาโดยอัตโนมัติเป็นตัวระบุประกันสังคมของพนักงานที่จำเป็นสำหรับการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="087b0-358">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-358">Primary (required)</span></span>
- <span data-ttu-id="087b0-359">ชนิดข้อมูลประจำตัว = "SSN"</span><span class="sxs-lookup"><span data-stu-id="087b0-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="087b0-360">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="087b0-360">Issued Date</span></span>
- <span data-ttu-id="087b0-361">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="087b0-361">Expiration Date</span></span>

<span data-ttu-id="087b0-362">พนักงานสามารถประกาศหมายเลขการระบุรหัสประจำตัวหลายเลขของชนิดการระบุรหัสประจำตัว **SSN**</span><span class="sxs-lookup"><span data-stu-id="087b0-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="087b0-363">อย่างไรก็ตาม เฉพาะเรกคอร์ดที่ถูกทำเครื่องหมายเป็น **หลัก** ถูกรวมเข้ากับ Dayforce ไม่ว่าหมายเลขจะใช้งานอยู่ หรือหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="087b0-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="087b0-364">บัญชีธนาคารและการเบิกจ่าย</span><span class="sxs-lookup"><span data-stu-id="087b0-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="087b0-365">ต้องป้อนข้อมูลบัญชีธนาคารที่ถูกต้องสำหรับพนักงานใดๆ ที่เลือกที่จะรับการชำระเงินผ่านการโอนย้ายของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="087b0-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="087b0-366">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-366">Human Resources</span></span>                         | <span data-ttu-id="087b0-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="087b0-368">หมายเลขบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="087b0-369">รหัส SWIFT (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-369">SWIFT code (required)</span></span>          | <span data-ttu-id="087b0-370">ฟิลด์ **รหัสธนาคาร** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="087b0-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="087b0-371">หมายเลขสาขา (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="087b0-372">ชนิดของบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-372">Bank account type (required)</span></span>   | <span data-ttu-id="087b0-373">ฟิลด์ **ชนิดของบัญชี** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="087b0-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="087b0-374">ค่าที่ได้รับการสนับสนุนได้แก่ **การตรวจสอบ** และ **ค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="087b0-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="087b0-375">พนักงานที่เลือกจะรับการชำระผ่านการโอนผ่านบัญชีธนาคาร ต้องมีลิงก์ไปยังบัญชีเงินส่วนที่เหลือที่อยู่ภายใต้นิติบุคคลที่มีที่อยู่หลักในเม็กซิโก และเชื่อมโยงกับบัญชีธนาคารที่ถูกต้องจากธนาคารเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="087b0-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="087b0-376">บัญชีที่ไม่ใช่เงินส่วนที่เหลืออื่นๆ ทั้งหมดจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="087b0-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="087b0-377">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="087b0-377">Address information</span></span>

<span data-ttu-id="087b0-378">พนักงานทุกคนต้องมีสถานที่หลักหนึ่งแห่ง</span><span class="sxs-lookup"><span data-stu-id="087b0-378">Every employee must have one primary location.</span></span> <span data-ttu-id="087b0-379">ใน Dayforce สถานที่นี้จะใช้เพื่อกำหนดที่พักอาศัยหลักของพนักงานสำหรับวัตถุประสงค์ด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="087b0-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="087b0-380">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-380">Primary (required)</span></span>
- <span data-ttu-id="087b0-381">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-381">Country/region (required)</span></span>
- <span data-ttu-id="087b0-382">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="087b0-383">ถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-383">Street (required)</span></span>
- <span data-ttu-id="087b0-384">หมายเลขถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-384">Street Number (required)</span></span>
- <span data-ttu-id="087b0-385">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="087b0-385">Building Complement</span></span>
- <span data-ttu-id="087b0-386">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-386">City (required)</span></span>
- <span data-ttu-id="087b0-387">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-387">State (required)</span></span>
- <span data-ttu-id="087b0-388">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="087b0-389">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="087b0-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="087b0-390">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในสหรัฐอเมริกาและแคนาดา ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="087b0-391">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-391">Departments are required on positions.</span></span>
- <span data-ttu-id="087b0-392">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="087b0-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="087b0-393">คุณสามารถตั้งค่าคอนฟิกทรัพยากรบุคคลเพื่อกำหนดว่าตำแหน่งต้องมีการระบุแผนก</span><span class="sxs-lookup"><span data-stu-id="087b0-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="087b0-394">เมื่อต้องการทำเช่นนี้ ไปยัง **ตำแหน่งที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล > ตำแหน่ง > ต้องการแผนกในตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="087b0-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="087b0-395">เราขอแนะนำให้ การตั้งค่านี้ถูกบังคับใช้สำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="087b0-396">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-396">Job types</span></span>

<span data-ttu-id="087b0-397">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="087b0-398">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="087b0-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="087b0-399">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="087b0-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="087b0-400">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="087b0-401">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="087b0-402">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-402">Job type</span></span>   | <span data-ttu-id="087b0-403">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="087b0-404">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="087b0-404">Hourly</span></span>     | <span data-ttu-id="087b0-405">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="087b0-405">Hourly</span></span>      |
| <span data-ttu-id="087b0-406">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-406">Salaried</span></span>   | <span data-ttu-id="087b0-407">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="087b0-408">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-408">Position types</span></span> 

<span data-ttu-id="087b0-409">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="087b0-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="087b0-410">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="087b0-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="087b0-411">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="087b0-412">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="087b0-412">Position type</span></span>   | <span data-ttu-id="087b0-413">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="087b0-414">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="087b0-414">Full-time</span></span>       | <span data-ttu-id="087b0-415">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="087b0-415">Full time employee</span></span> |
| <span data-ttu-id="087b0-416">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="087b0-416">Part-time</span></span>       | <span data-ttu-id="087b0-417">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="087b0-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="087b0-418">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="087b0-418">Reason codes</span></span>

<span data-ttu-id="087b0-419">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="087b0-420">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="087b0-421">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="087b0-422">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="087b0-422">Reason code</span></span>    | <span data-ttu-id="087b0-423">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-423">Description</span></span>      | <span data-ttu-id="087b0-424">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="087b0-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="087b0-425">การลาออก</span><span class="sxs-lookup"><span data-stu-id="087b0-425">RESIGNATION</span></span>    | <span data-ttu-id="087b0-426">การลาออก</span><span class="sxs-lookup"><span data-stu-id="087b0-426">Resignation</span></span>      | <span data-ttu-id="087b0-427">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-427">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-428">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-428">TERMINATION</span></span>    | <span data-ttu-id="087b0-429">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-429">Termination</span></span>      | <span data-ttu-id="087b0-430">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-430">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-431">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="087b0-431">RETIREMENT</span></span>     | <span data-ttu-id="087b0-432">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="087b0-432">Retirement</span></span>       | <span data-ttu-id="087b0-433">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-433">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-434">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-434">OTHER</span></span>          | <span data-ttu-id="087b0-435">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-435">Other Reasons</span></span>    | <span data-ttu-id="087b0-436">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-436">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-437">ความตาย</span><span class="sxs-lookup"><span data-stu-id="087b0-437">DEATH</span></span>          | <span data-ttu-id="087b0-438">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="087b0-438">Death</span></span>            | <span data-ttu-id="087b0-439">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-439">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="087b0-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="087b0-441">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="087b0-441">Leave of Absence</span></span> | <span data-ttu-id="087b0-442">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-442">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="087b0-443">CONTRACTEND</span></span>    | <span data-ttu-id="087b0-444">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="087b0-444">End of Contract</span></span>  | <span data-ttu-id="087b0-445">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-445">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="087b0-446">SALARYCHANGE</span></span>   | <span data-ttu-id="087b0-447">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-447">Change of Salary</span></span> | <span data-ttu-id="087b0-448">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="087b0-449">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="087b0-449">Marital status</span></span>

<span data-ttu-id="087b0-450">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="087b0-451">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="087b0-452">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-452">Human Resources</span></span>                 | <span data-ttu-id="087b0-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="087b0-454">สมรส</span><span class="sxs-lookup"><span data-stu-id="087b0-454">Married</span></span>                | <span data-ttu-id="087b0-455">สมรส</span><span class="sxs-lookup"><span data-stu-id="087b0-455">Married</span></span>              |
| <span data-ttu-id="087b0-456">โสด</span><span class="sxs-lookup"><span data-stu-id="087b0-456">Single</span></span>                 | <span data-ttu-id="087b0-457">โสด</span><span class="sxs-lookup"><span data-stu-id="087b0-457">Single</span></span>               |
| <span data-ttu-id="087b0-458">หม้าย</span><span class="sxs-lookup"><span data-stu-id="087b0-458">Widowed</span></span>                | <span data-ttu-id="087b0-459">หม้าย</span><span class="sxs-lookup"><span data-stu-id="087b0-459">Widowed</span></span>              |
| <span data-ttu-id="087b0-460">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-460">Divorced</span></span>               | <span data-ttu-id="087b0-461">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-461">Divorced</span></span>             |
| <span data-ttu-id="087b0-462">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="087b0-462">Registered Partnership</span></span> | <span data-ttu-id="087b0-463">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="087b0-463">Domestic Partnership</span></span> |
| <span data-ttu-id="087b0-464">None</span><span class="sxs-lookup"><span data-stu-id="087b0-464">None</span></span>                   | <span data-ttu-id="087b0-465">None</span><span class="sxs-lookup"><span data-stu-id="087b0-465">None</span></span>                 |
| <span data-ttu-id="087b0-466">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="087b0-466">Cohabiting</span></span>             | <span data-ttu-id="087b0-467">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="087b0-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="087b0-468">เพศ</span><span class="sxs-lookup"><span data-stu-id="087b0-468">Gender</span></span>

<span data-ttu-id="087b0-469">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="087b0-470">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="087b0-471">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-471">Human Resources</span></span>       | <span data-ttu-id="087b0-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="087b0-473">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="087b0-473">Male</span></span>         | <span data-ttu-id="087b0-474">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="087b0-474">Male</span></span>            |
| <span data-ttu-id="087b0-475">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="087b0-475">Female</span></span>       | <span data-ttu-id="087b0-476">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="087b0-476">Female</span></span>          |
| <span data-ttu-id="087b0-477">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="087b0-477">Non-specific</span></span> | <span data-ttu-id="087b0-478">*ไม่สนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="087b0-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="087b0-479">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-479">Earning codes</span></span>

<span data-ttu-id="087b0-480">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="087b0-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="087b0-481">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="087b0-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="087b0-482">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="087b0-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="087b0-483">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="087b0-483">Supported frequencies</span></span>

- <span data-ttu-id="087b0-484">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="087b0-484">All</span></span>
- <span data-ttu-id="087b0-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="087b0-485">EVERYPAY</span></span>
- <span data-ttu-id="087b0-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="087b0-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="087b0-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="087b0-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="087b0-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="087b0-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="087b0-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-489">1OFMTH</span></span>
- <span data-ttu-id="087b0-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-490">LASTOFMTH</span></span>
- <span data-ttu-id="087b0-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-491">2OFMTH</span></span>
- <span data-ttu-id="087b0-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-492">3OFMTH</span></span>
- <span data-ttu-id="087b0-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-493">4OFMTH</span></span>
- <span data-ttu-id="087b0-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-494">5OFMTH</span></span>
- <span data-ttu-id="087b0-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-495">1N2OFMTH</span></span>
- <span data-ttu-id="087b0-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-496">3N4OFMTH</span></span>
- <span data-ttu-id="087b0-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-497">1N3OFMTH</span></span>
- <span data-ttu-id="087b0-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-498">1N4OFMTH</span></span>
- <span data-ttu-id="087b0-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-499">2N3OFMTH</span></span>
- <span data-ttu-id="087b0-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-500">2N4OFMTH</span></span>
- <span data-ttu-id="087b0-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="087b0-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="087b0-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="087b0-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="087b0-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="087b0-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="087b0-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="087b0-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="087b0-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="087b0-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="087b0-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="087b0-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="087b0-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="087b0-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="087b0-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="087b0-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="087b0-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="087b0-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="087b0-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="087b0-513">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="087b0-513">Addresses</span></span>

<span data-ttu-id="087b0-514">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="087b0-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="087b0-515">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="087b0-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="087b0-516">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-516">Human Resources</span></span>          | <span data-ttu-id="087b0-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="087b0-518">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="087b0-518">Country/Region</span></span>  | <span data-ttu-id="087b0-519">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="087b0-519">Country Code</span></span>          |
| <span data-ttu-id="087b0-520">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="087b0-520">Zip/Postal Code</span></span> | <span data-ttu-id="087b0-521">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="087b0-521">Postal Code</span></span>           |
| <span data-ttu-id="087b0-522">สถานะ</span><span class="sxs-lookup"><span data-stu-id="087b0-522">State</span></span>           | <span data-ttu-id="087b0-523">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="087b0-523">State Code</span></span>            |
| <span data-ttu-id="087b0-524">เมือง</span><span class="sxs-lookup"><span data-stu-id="087b0-524">City</span></span>            | <span data-ttu-id="087b0-525">เมือง</span><span class="sxs-lookup"><span data-stu-id="087b0-525">City</span></span>                  |
| <span data-ttu-id="087b0-526">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="087b0-526">County</span></span>          | <span data-ttu-id="087b0-527">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="087b0-527">County (Municipality)</span></span> |
| <span data-ttu-id="087b0-528">ถนน</span><span class="sxs-lookup"><span data-stu-id="087b0-528">Street</span></span>          | <span data-ttu-id="087b0-529">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="087b0-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="087b0-530">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="087b0-530">Tax regions</span></span>

<span data-ttu-id="087b0-531">ภูมิภาคการเก็บภาษีถูกใช้เพื่อกำหนดภาษีที่เหมาะสมที่ควรนำมาใช้ในระหว่างการสร้างระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="087b0-532">ภูมิภาคการเก็บภาษีถูกแม็ปไปยัง Dayforce เป็นที่อยู่ของสถานที่</span><span class="sxs-lookup"><span data-stu-id="087b0-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="087b0-533">ภูมิภาคการเก็บภาษีเริ่มต้นต้องเชื่อมโยงกับตำแหน่งงานที่ใช้งานอยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="087b0-534">ภูมิภาคการเก็บภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-534">Tax region (required)</span></span>
- <span data-ttu-id="087b0-535">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-535">Country/Region (required)</span></span>
- <span data-ttu-id="087b0-536">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-536">State (required)</span></span>
- <span data-ttu-id="087b0-537">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="087b0-537">County</span></span> 
- <span data-ttu-id="087b0-538">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="087b0-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="087b0-539">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="087b0-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="087b0-540">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในเม็กซิโก ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="087b0-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="087b0-541">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-541">Departments are required on positions.</span></span>
- <span data-ttu-id="087b0-542">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="087b0-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="087b0-543">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-543">Job types</span></span>

<span data-ttu-id="087b0-544">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="087b0-545">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="087b0-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="087b0-546">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="087b0-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="087b0-547">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="087b0-548">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="087b0-549">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-549">Job type</span></span>   | <span data-ttu-id="087b0-550">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="087b0-551">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="087b0-551">Hourly</span></span>     | <span data-ttu-id="087b0-552">MX รายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="087b0-552">MX Hourly</span></span>   |
| <span data-ttu-id="087b0-553">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-553">Salaried</span></span>   | <span data-ttu-id="087b0-554">MX รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="087b0-555">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-555">Position types</span></span> 

<span data-ttu-id="087b0-556">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="087b0-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="087b0-557">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="087b0-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="087b0-558">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="087b0-559">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="087b0-559">Position type</span></span>   | <span data-ttu-id="087b0-560">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="087b0-561">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="087b0-561">Full-time</span></span>       | <span data-ttu-id="087b0-562">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="087b0-562">Full time employee</span></span> |
| <span data-ttu-id="087b0-563">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="087b0-563">Part-time</span></span>       | <span data-ttu-id="087b0-564">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="087b0-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="087b0-565">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="087b0-565">Reason codes</span></span>

<span data-ttu-id="087b0-566">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="087b0-567">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="087b0-568">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="087b0-569">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="087b0-569">Reason code</span></span>            | <span data-ttu-id="087b0-570">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-570">Description</span></span>                    | <span data-ttu-id="087b0-571">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="087b0-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="087b0-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="087b0-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="087b0-573">การออกก่อนค่าจ้างแรก</span><span class="sxs-lookup"><span data-stu-id="087b0-573">Departure before first payroll</span></span> | <span data-ttu-id="087b0-574">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-574">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-575">การลาออก</span><span class="sxs-lookup"><span data-stu-id="087b0-575">RESIGNATION</span></span>            | <span data-ttu-id="087b0-576">การลาออก</span><span class="sxs-lookup"><span data-stu-id="087b0-576">Resignation</span></span>                    | <span data-ttu-id="087b0-577">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-577">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-578">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="087b0-578">PENSION</span></span>                | <span data-ttu-id="087b0-579">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="087b0-579">Pension</span></span>                        | <span data-ttu-id="087b0-580">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-580">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-581">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-581">TERMINATION</span></span>            | <span data-ttu-id="087b0-582">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-582">Termination</span></span>                    | <span data-ttu-id="087b0-583">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-583">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-584">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="087b0-584">RETIREMENT</span></span>             | <span data-ttu-id="087b0-585">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="087b0-585">Retirement</span></span>                     | <span data-ttu-id="087b0-586">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-586">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-587">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-587">ABSENTEE</span></span>               | <span data-ttu-id="087b0-588">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-588">Absentee</span></span>                       | <span data-ttu-id="087b0-589">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-589">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-590">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-590">OTHER</span></span>                  | <span data-ttu-id="087b0-591">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-591">Other Reasons</span></span>                  | <span data-ttu-id="087b0-592">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-592">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-593">การปิด</span><span class="sxs-lookup"><span data-stu-id="087b0-593">CLOSURE</span></span>                | <span data-ttu-id="087b0-594">การปิดของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="087b0-594">Business Closure</span></span>               | <span data-ttu-id="087b0-595">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-595">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-596">ความตาย</span><span class="sxs-lookup"><span data-stu-id="087b0-596">DEATH</span></span>                  | <span data-ttu-id="087b0-597">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="087b0-597">Death</span></span>                          | <span data-ttu-id="087b0-598">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-598">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="087b0-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="087b0-600">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="087b0-600">Leave of Absence</span></span>               | <span data-ttu-id="087b0-601">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-601">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="087b0-602">CONTRACTEND</span></span>            | <span data-ttu-id="087b0-603">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="087b0-603">End of Contract</span></span>                | <span data-ttu-id="087b0-604">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-604">Terminate worker</span></span>     |
| <span data-ttu-id="087b0-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="087b0-605">SALARYCHANGE</span></span>           | <span data-ttu-id="087b0-606">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="087b0-606">Change of Salary</span></span>               | <span data-ttu-id="087b0-607">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="087b0-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="087b0-608">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-608">Terms of employment</span></span>

<span data-ttu-id="087b0-609">มีการใช้เงื่อนไขของการจ้างงาน เพื่อสร้างประเภทและตัวอย่างของการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="087b0-610">เงื่อนไขถูกแม็ปกับ Dayforce เป็นค่าตัวบ่งชี้การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="087b0-611">เงื่อนไขการจ้างงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="087b0-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="087b0-612">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-612">Terms of employment</span></span>   | <span data-ttu-id="087b0-613">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="087b0-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="087b0-614">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="087b0-614">Regular</span></span>               | <span data-ttu-id="087b0-615">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="087b0-615">Regular</span></span>     |
| <span data-ttu-id="087b0-616">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="087b0-616">Direct</span></span>                | <span data-ttu-id="087b0-617">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="087b0-617">Direct</span></span>      |
| <span data-ttu-id="087b0-618">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-618">Internship</span></span>            | <span data-ttu-id="087b0-619">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-619">Internship</span></span>  |
| <span data-ttu-id="087b0-620">ถาวร</span><span class="sxs-lookup"><span data-stu-id="087b0-620">Permanent</span></span>             | <span data-ttu-id="087b0-621">ถาวร</span><span class="sxs-lookup"><span data-stu-id="087b0-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="087b0-622">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="087b0-622">Marital status</span></span>

<span data-ttu-id="087b0-623">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="087b0-624">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="087b0-625">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-625">Human Resources</span></span>                 | <span data-ttu-id="087b0-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="087b0-627">สมรส</span><span class="sxs-lookup"><span data-stu-id="087b0-627">Married</span></span>                | <span data-ttu-id="087b0-628">สมรส</span><span class="sxs-lookup"><span data-stu-id="087b0-628">Married</span></span>                   |
| <span data-ttu-id="087b0-629">โสด</span><span class="sxs-lookup"><span data-stu-id="087b0-629">Single</span></span>                 | <span data-ttu-id="087b0-630">โสด</span><span class="sxs-lookup"><span data-stu-id="087b0-630">Single</span></span>                    |
| <span data-ttu-id="087b0-631">หม้าย</span><span class="sxs-lookup"><span data-stu-id="087b0-631">Widowed</span></span>                | <span data-ttu-id="087b0-632">หม้าย</span><span class="sxs-lookup"><span data-stu-id="087b0-632">Widowed</span></span>                   |
| <span data-ttu-id="087b0-633">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-633">Divorced</span></span>               | <span data-ttu-id="087b0-634">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-634">Divorced</span></span>                  |
| <span data-ttu-id="087b0-635">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="087b0-635">Registered Partnership</span></span> | <span data-ttu-id="087b0-636">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="087b0-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="087b0-637">None</span><span class="sxs-lookup"><span data-stu-id="087b0-637">None</span></span>                   | <span data-ttu-id="087b0-638">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="087b0-639">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="087b0-639">Cohabiting</span></span>             | <span data-ttu-id="087b0-640">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="087b0-641">เพศ</span><span class="sxs-lookup"><span data-stu-id="087b0-641">Gender</span></span>

<span data-ttu-id="087b0-642">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="087b0-643">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="087b0-644">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-644">Human Resources</span></span>       | <span data-ttu-id="087b0-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="087b0-646">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="087b0-646">Male</span></span>         | <span data-ttu-id="087b0-647">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="087b0-647">Male</span></span>                      |
| <span data-ttu-id="087b0-648">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="087b0-648">Female</span></span>       | <span data-ttu-id="087b0-649">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="087b0-649">Female</span></span>                    |
| <span data-ttu-id="087b0-650">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="087b0-650">Non-specific</span></span> | <span data-ttu-id="087b0-651">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="087b0-652">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="087b0-652">Payment method</span></span>

<span data-ttu-id="087b0-653">วิธีการชำระเงินให้พนักงานและบริษัทมีวิธีในการอธิบายวิธีการจ่ายเงินแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="087b0-654">วิธีการชำระเงินถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="087b0-655">ตารางต่อไปนี้แสดงวิธีการแม็ปวิธีการชำระเงินกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="087b0-656">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-656">Human Resources</span></span>             | <span data-ttu-id="087b0-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="087b0-658">เงินสด</span><span class="sxs-lookup"><span data-stu-id="087b0-658">Cash</span></span>               | <span data-ttu-id="087b0-659">เงินสด</span><span class="sxs-lookup"><span data-stu-id="087b0-659">Cash</span></span>                      |
| <span data-ttu-id="087b0-660">การชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="087b0-660">Electronic Payment</span></span> | <span data-ttu-id="087b0-661">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="087b0-661">Transfer</span></span>                  |
| <span data-ttu-id="087b0-662">ตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="087b0-662">Check</span></span>              | <span data-ttu-id="087b0-663">เช็ค</span><span class="sxs-lookup"><span data-stu-id="087b0-663">Cheque</span></span>                    |
| <span data-ttu-id="087b0-664">ตั๋วแลกเงินธนาคาร</span><span class="sxs-lookup"><span data-stu-id="087b0-664">Bank Draft</span></span>         | <span data-ttu-id="087b0-665">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="087b0-666">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="087b0-666">Other</span></span>              | <span data-ttu-id="087b0-667">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="087b0-668">ชนิดของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="087b0-668">Bank account type</span></span>

<span data-ttu-id="087b0-669">ชนิดของบัญชีธนาคารถูกใช้สำหรับการชำระเงินทางอิเล็กทรอนิกส์แก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="087b0-670">ชนิดบัญชีธนาคารถูกแม็ปกับ Dayforce เป็นข้อมูลบัญชีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="087b0-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="087b0-671">ชนิดของบัญชีธนาคารจะถูกแปล ตามความเหมาะสม กับค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="087b0-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="087b0-672">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-672">Human Resources</span></span>            | <span data-ttu-id="087b0-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="087b0-674">บัญชีกระแสรายวัน</span><span class="sxs-lookup"><span data-stu-id="087b0-674">Checking Account</span></span>  | <span data-ttu-id="087b0-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="087b0-675">CheckingAccount</span></span>           |
| <span data-ttu-id="087b0-676">บัญชีเครดิตค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="087b0-676">Payroll Account</span></span>   | <span data-ttu-id="087b0-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="087b0-677">PayrollAccount</span></span>            |
| <span data-ttu-id="087b0-678">บัญชีออมทรัพย์</span><span class="sxs-lookup"><span data-stu-id="087b0-678">Savings Account</span></span>   | <span data-ttu-id="087b0-679">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="087b0-680">บัญชี BankGirot</span><span class="sxs-lookup"><span data-stu-id="087b0-680">BankGirot account</span></span> | <span data-ttu-id="087b0-681">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="087b0-682">บัญชี PlusGirot</span><span class="sxs-lookup"><span data-stu-id="087b0-682">PlusGirot account</span></span> | <span data-ttu-id="087b0-683">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="087b0-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="087b0-684">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="087b0-684">Earning codes</span></span>

<span data-ttu-id="087b0-685">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="087b0-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="087b0-686">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="087b0-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="087b0-687">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="087b0-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="087b0-688">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="087b0-688">Supported frequencies</span></span>

- <span data-ttu-id="087b0-689">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="087b0-689">All</span></span>
- <span data-ttu-id="087b0-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="087b0-690">EVERYPAY</span></span>
- <span data-ttu-id="087b0-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="087b0-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="087b0-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="087b0-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="087b0-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="087b0-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="087b0-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-694">1OFMTH</span></span>
- <span data-ttu-id="087b0-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-695">LASTOFMTH</span></span>
- <span data-ttu-id="087b0-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-696">2OFMTH</span></span>
- <span data-ttu-id="087b0-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-697">3OFMTH</span></span>
- <span data-ttu-id="087b0-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-698">4OFMTH</span></span>
- <span data-ttu-id="087b0-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-699">5OFMTH</span></span>
- <span data-ttu-id="087b0-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-700">1N2OFMTH</span></span>
- <span data-ttu-id="087b0-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-701">3N4OFMTH</span></span>
- <span data-ttu-id="087b0-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-702">1N3OFMTH</span></span>
- <span data-ttu-id="087b0-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-703">1N4OFMTH</span></span>
- <span data-ttu-id="087b0-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-704">2N3OFMTH</span></span>
- <span data-ttu-id="087b0-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-705">2N4OFMTH</span></span>
- <span data-ttu-id="087b0-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="087b0-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="087b0-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="087b0-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="087b0-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="087b0-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="087b0-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="087b0-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="087b0-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="087b0-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="087b0-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="087b0-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="087b0-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="087b0-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="087b0-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="087b0-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="087b0-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="087b0-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="087b0-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="087b0-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="087b0-718">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="087b0-718">Addresses</span></span>

<span data-ttu-id="087b0-719">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="087b0-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="087b0-720">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="087b0-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="087b0-721">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="087b0-721">Human Resources</span></span>              | <span data-ttu-id="087b0-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="087b0-723">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="087b0-723">Country/Region</span></span>      | <span data-ttu-id="087b0-724">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="087b0-724">Country Code</span></span>          |
| <span data-ttu-id="087b0-725">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="087b0-725">Zip/Postal Code</span></span>     | <span data-ttu-id="087b0-726">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="087b0-726">Postal Code</span></span>           |
| <span data-ttu-id="087b0-727">สถานะ</span><span class="sxs-lookup"><span data-stu-id="087b0-727">State</span></span>               | <span data-ttu-id="087b0-728">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="087b0-728">State Code</span></span>            |
| <span data-ttu-id="087b0-729">เมือง</span><span class="sxs-lookup"><span data-stu-id="087b0-729">City</span></span>                | <span data-ttu-id="087b0-730">เมือง</span><span class="sxs-lookup"><span data-stu-id="087b0-730">City</span></span>                  |
| <span data-ttu-id="087b0-731">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="087b0-731">County</span></span>              | <span data-ttu-id="087b0-732">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="087b0-732">County (Municipality)</span></span> |
| <span data-ttu-id="087b0-733">ถนน</span><span class="sxs-lookup"><span data-stu-id="087b0-733">Street</span></span>              | <span data-ttu-id="087b0-734">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="087b0-734">Address Line 1</span></span>        |
| <span data-ttu-id="087b0-735">หมายเลขถนน</span><span class="sxs-lookup"><span data-stu-id="087b0-735">Street Number</span></span>       | <span data-ttu-id="087b0-736">ที่อยู่ บรรทัดที่ 2</span><span class="sxs-lookup"><span data-stu-id="087b0-736">Address Line 2</span></span>        |
| <span data-ttu-id="087b0-737">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="087b0-737">Building Complement</span></span> | <span data-ttu-id="087b0-738">ที่อยู่ บรรทัดที่ 5</span><span class="sxs-lookup"><span data-stu-id="087b0-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="087b0-739">หมายเลขหนังสือเดินทาง</span><span class="sxs-lookup"><span data-stu-id="087b0-739">Passport number</span></span>

<span data-ttu-id="087b0-740">พนักงานสามารถประกาศข้อมูลหนังสือเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="087b0-740">Employees can declare passport information.</span></span> <span data-ttu-id="087b0-741">ข้อมูลนี้เป็นชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง** และถูกรวมอยู่ใน Dayforce เป็นส่วนหนึ่งของข้อมูลเม็กซิโกเฉพาะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="087b0-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="087b0-742">ชนิดการระบุรหัสประจำตัว = "หนังสือเดินทาง"</span><span class="sxs-lookup"><span data-stu-id="087b0-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="087b0-743">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="087b0-743">Issued Date</span></span>
- <span data-ttu-id="087b0-744">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="087b0-744">Expiration Date</span></span>

<span data-ttu-id="087b0-745">พนักงานสามารถประกาศหมายเลขรหัสหลายเลขของชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="087b0-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="087b0-746">อย่างไรก็ตาม เฉพาะรายการหนังสือเดินทางที่ใช้งานปัจจุบันจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="087b0-747">ถ้ารายการหนังสือเดินทางทั้งหมดหมดอายุ หนังสือเดินทางที่ออกครั้งล่าสุดจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="087b0-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

