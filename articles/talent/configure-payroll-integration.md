---
title: ตั้งค่าคอนฟิกการรวมค่าจ้างระหว่าง Talent และ Dayforce
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการรวมระหว่าง Microsoft Dynamics 365 Talent และ Ceridian Dayforce เพื่อให้คุณสามารถประมวลผลการรันค่าจ้าง
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898554"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="5b47e-103">ตั้งค่าคอนฟิกการรวมระบบค่าจ้างระหว่าง Talent และ Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="5b47e-104">การรวมระหว่าง Microsoft Dynamics 365 Talent และ Ceridian Dayforce ขึ้นอยู่กับขั้นตอนการตั้งค่าคอนฟิกหลายขั้นตอนที่ถูกอธิบายไว้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="5b47e-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="5b47e-105">คุณต้องตั้งค่าคอนฟิกการรวมทั้ง Talent และ Dayforce ก่อนที่คุณจะสามารถประมวลผลการชำระค่าจ้างที่รันได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="5b47e-106">เมื่อคุณใช้บริการเช่น Dayforce เพื่อทำให้การชำระค่าจ้างเสร็จสมบูรณ์ คุณต้องเปิดใช้งานการรวมใน Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="5b47e-107">การรวมจำเป็นต้องมีข้อมูลที่เฉพาะเจาะจงจาก Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="5b47e-108">ดังนั้น คุณต้องตรวจสอบว่า ข้อมูลที่มีการแม็ปกับ Dayforce ถูกตั้งค่าคอนฟิกใน Talent ในลักษณะที่สนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="5b47e-109">การรวมใช้ประเภทที่กว้างของข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="5b47e-110">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5b47e-110">Human resources data</span></span>
- <span data-ttu-id="5b47e-111">ข้อมูลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-111">Compensation data</span></span>
- <span data-ttu-id="5b47e-112">ข้อมูลค่าจ้าง เช่น รอบการชำระค่าจ้าง รอบระยะเวลาการชำระค่าจ้าง และรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="5b47e-113">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-113">Worker data</span></span>

<span data-ttu-id="5b47e-114">หัวข้อนี้อธิบายขั้นตอนต่างๆ ที่คุณต้องปฏิบัติตามเพื่อเปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="5b47e-115">นอกจากนี้ ยังอธิบายถึงชนิดของข้อมูลและรายละเอียดการตั้งค่าคอนฟิกที่การรวมต้องการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="5b47e-116">เปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-116">Enable the integration</span></span>

<span data-ttu-id="5b47e-117">ใน Talent คุณต้องเปิดใช้งานการรวม และป้อนข้อมูลการตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="5b47e-118">ถ้าคุณต้องการธุรกรรมบัญชีแยกประเภททั่วไปที่ถูกผลิตให้ถูกนำเข้าลงใน Microsoft Dynamics 365 Finance คุณยังต้องตั้งค่าบัญชีที่จัดเก็บ Microsoft Azure และป้อนสตริงการเชื่อมต่อที่จัดเก็บ Azure ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b47e-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="5b47e-119">เมื่อต้องการเปิดใช้งานการรวมใน Talent ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5b47e-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="5b47e-120">ในหน้า **การดูแลระบบ** เลือก **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="5b47e-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="5b47e-121">ป้อนปลายทาง File Transfer Protocol (FTP) แบบปลอดภัย และพาธโฟลเดอร์ FTP แบบปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5b47e-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="5b47e-122">ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่จะเข้าถึงปลายทาง FTP แบบปลอดภัย และโฟลเดอร์พาธ</span><span class="sxs-lookup"><span data-stu-id="5b47e-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="5b47e-123">ทดสอบการเชื่อมต่อ หากจำเป็น และตั้งค่าตัวเลือก **เปิดใช้งานการรวมค่าจ้าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="5b47e-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="5b47e-124">เมื่อเปิดการรวม มีการสร้างแพคเกจการส่งออกข้อมูลและไฟล์ และมีการตั้งค่าความถี่</span><span class="sxs-lookup"><span data-stu-id="5b47e-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="5b47e-125">คุณสามารถเปลี่ยนความถี่นี้ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="5b47e-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบัญชีการจัดเก็บ Azure และสตริงการเชื่อมต่อการจัดเก็บ Azure ดูหัวข้อ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="5b47e-127">เกี่ยวกับบัญชีการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="5b47e-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="5b47e-128">ตั้งค่าคอนฟิกสตริงการเชื่อมต่อการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="5b47e-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="5b47e-129">รายละเอียดทางเทคนิค เมื่อเปิดใช้งานการรวมค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="5b47e-130">การเปิดการรวมค่าจ้างมีผลกระทบหลักสองประการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="5b47e-131">โครงการส่งออกข้อมูลที่มีชื่อว่า "การส่งออกการรวมค่าจ้าง" ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="5b47e-132">โครงการนี้ประกอบด้วยเอนทิตีและฟิลด์ที่จำเป็นสำหรับการรวมค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="5b47e-133">เมื่อต้องการตรวจสอบโครงการ ให้ไปที่ **การจัดการระบบ** เลือกไทล์ **การจัดการข้อมูล** แล้วเปิดโครงการข้อมูลจากรายการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="5b47e-134">ชุดงานนี้จะดำเนินการโครงการส่งออกข้อมูล เข้ารหัสแพคเกจข้อมูลที่เป็นผลลัพธ์ และโอนย้ายไฟล์แพคเกจข้อมูลไปยังปลายทาง SFTP ที่ตั้งค่าคอนฟิกบนหน้าจอ **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="5b47e-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="5b47e-135">แพคเกจข้อมูลที่โอนย้ายไปยังปลายทาง SFTP ถูกเข้ารหัสโดยใช้คีย์ที่ไม่ซ้ำกันสำหรับแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="5b47e-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="5b47e-136">คีย์อยู่ใน Azure Key Vault ที่สามารถเข้าถึงได้โดย Ceridian เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="5b47e-137">ไม่สามารถถอดรหัสและตรวจสอบเนื้อหาของแพคเกจข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="5b47e-138">ถ้าคุณต้องการตรวจสอบเนื้อหาของแพคเกจข้อมูล คุณต้องส่งออกโครงการข้อมูล "การส่งออกการรวมบัญชีค่าจ้าง" ด้วยตนเอง ให้ดาวน์โหลดโครงการนั้น แล้วเปิด</span><span class="sxs-lookup"><span data-stu-id="5b47e-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="5b47e-139">การส่งออกด้วยตนเองจะไม่ใช้การเข้ารหัสหรือโอนย้ายบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5b47e-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="5b47e-140">ตั้งค่าคอนฟิกข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-140">Configure your data</span></span> 

<span data-ttu-id="5b47e-141">ในการประมวลผลค่าจ้าง คุณต้องตั้งค่าคอนฟิกข้อมูลทรัพยากรบุคคลใน Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="5b47e-142">คุณต้องตั้งค่าข้อมูลองค์กร เช่น งาน และตำแหน่ง พร้อมด้วยข้อมูลค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="5b47e-143">ข้อมูลนี้ให้ข้อมูลการจ้างงาน ค่าจ้าง และการหักลด ที่จำเป็นในการสร้างค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="5b47e-144">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5b47e-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="5b47e-145">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-145">Benefits</span></span> 

<span data-ttu-id="5b47e-146">ทรัพยากรบุคคลให้เครื่องมือสำหรับการตั้งค่าและการบำรุงรักษาของสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงาน ที่หน่วยงานนำเสนอหรือประมวลผลสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="5b47e-147">เมื่อคุณสร้างสวัสดิการ พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="5b47e-148">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-148">Benefit plans</span></span>

- <span data-ttu-id="5b47e-149">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-149">Plan (required)</span></span>
- <span data-ttu-id="5b47e-150">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-150">Type (required)</span></span>
- <span data-ttu-id="5b47e-151">ผลกระทบของค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-151">Payroll impact (required)</span></span>
- <span data-ttu-id="5b47e-152">ขอคืนเงินค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="5b47e-152">Recover arrears</span></span>
- <span data-ttu-id="5b47e-153">วิธีการหักลด</span><span class="sxs-lookup"><span data-stu-id="5b47e-153">Deduction method</span></span>
- <span data-ttu-id="5b47e-154">ระดับความสำคัญการหักลด</span><span class="sxs-lookup"><span data-stu-id="5b47e-154">Deduction priority</span></span>
- <span data-ttu-id="5b47e-155">จำกัดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="5b47e-155">Limit period</span></span>
- <span data-ttu-id="5b47e-156">ยอดวงเงิน</span><span class="sxs-lookup"><span data-stu-id="5b47e-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="5b47e-157">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-157">Benefits</span></span>

- <span data-ttu-id="5b47e-158">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-158">Plan (required)</span></span>
- <span data-ttu-id="5b47e-159">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-159">Type (required)</span></span>
- <span data-ttu-id="5b47e-160">ตัวเลือก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-160">Option (required)</span></span>
- <span data-ttu-id="5b47e-161">รหัสสวัสดิการ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-161">Benefit ID (required)</span></span>
- <span data-ttu-id="5b47e-162">ความถี่</span><span class="sxs-lookup"><span data-stu-id="5b47e-162">Frequency</span></span>
- <span data-ttu-id="5b47e-163">ข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-163">Basis</span></span>
- <span data-ttu-id="5b47e-164">ยอดเงินหรืออัตรา</span><span class="sxs-lookup"><span data-stu-id="5b47e-164">Amount or rate</span></span>
- <span data-ttu-id="5b47e-165">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="5b47e-166">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5b47e-166">Supported frequencies</span></span> 

- <span data-ttu-id="5b47e-167">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="5b47e-167">Weekly</span></span>
- <span data-ttu-id="5b47e-168">ทุกสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="5b47e-168">Bi-weekly</span></span>
- <span data-ttu-id="5b47e-169">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-169">Semi-monthly</span></span>
- <span data-ttu-id="5b47e-170">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="5b47e-171">ฐานที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5b47e-171">Supported bases</span></span> 

- <span data-ttu-id="5b47e-172">ยอดเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-172">Fixed amount</span></span>
- <span data-ttu-id="5b47e-173">เปอร์เซ็นต์ของรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-173">Percent of earnings</span></span>
- <span data-ttu-id="5b47e-174">ชั่วโมงที่มีประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-174">Productive hours</span></span>

<span data-ttu-id="5b47e-175">Dayforce สร้างการหักลดต่อไปนี้ โดยขึ้นอยู่กับผลกระทบของค่าจ้างที่กำหนดในแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="5b47e-176">การเลือกใน Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-176">Selection in Talent</span></span>        | <span data-ttu-id="5b47e-177">ผลลัพธ์ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="5b47e-178">None</span><span class="sxs-lookup"><span data-stu-id="5b47e-178">None</span></span>                       | <span data-ttu-id="5b47e-179">ไม่มีการสร้างการหักลด</span><span class="sxs-lookup"><span data-stu-id="5b47e-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="5b47e-180">การหักลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-180">Deduction only</span></span>             | <span data-ttu-id="5b47e-181">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="5b47e-182">การจ่ายเงินสมทบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-182">Contribution only</span></span>          | <span data-ttu-id="5b47e-183">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="5b47e-184">การหักลดและการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="5b47e-184">Deduction and contribution</span></span> | <span data-ttu-id="5b47e-185">การหักลดพนักงานและนายจ้างจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="5b47e-186">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนด และจัดการโปรแกรมสวัสดิการ ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="5b47e-187">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="5b47e-188">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="5b47e-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="5b47e-189">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="5b47e-190">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="5b47e-191">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-191">Compensation</span></span> 

<span data-ttu-id="5b47e-192">การจัดการค่าตอบแทนจะใช้ควบคุมการจัดส่งของค่าจ้างพื้นฐานและเงินรางวัล</span><span class="sxs-lookup"><span data-stu-id="5b47e-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="5b47e-193">ค่าจ้างพื้นฐานคงที่ของพนักงานและการขึ้นค่าตอบแทนตามผลงานจะถูกควบคุมโดยใช้แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="5b47e-194">ค่าจ้างจูงใจเช่นการชำระเงินโบนัส รางวัลตามผลการปฏิบัติงาน สิทธิในการซื้อหุ้น การให้หุ้น รางวัลที่จ่ายครั้งเดียว โดยใช้แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5b47e-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="5b47e-195">Dayforce ใช้ข้อมูลค่าตอบแทนที่คำนวณอัตรารายชั่วโมงหรือรายปีของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="5b47e-196">จำเป็นต้องมีแผนค่าตอบแทนคงที่และการแปลงอัตราค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="5b47e-197">พนักงานต้องเชื่อมโยงกับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="5b47e-198">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแผนค่าตอบแทน โปรดดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="5b47e-199">สร้างแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="5b47e-200">สร้างแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5b47e-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="5b47e-201">พัฒนาโครงสร้างและแผนเงินเดือน/ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="5b47e-202">ประมวลผลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="5b47e-203">กำหนดกระบวนการของค่าตอบแทนและคำนวณผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5b47e-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="5b47e-204">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="5b47e-205">การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="5b47e-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="5b47e-206">งาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-206">Jobs</span></span> 

<span data-ttu-id="5b47e-207">งานเป็นชุดของงานและความรับผิดชอบที่ถูกระบุของบุคคลที่ดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="5b47e-208">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="5b47e-209">การตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="5b47e-210">กำหนดงานใหม่</span><span class="sxs-lookup"><span data-stu-id="5b47e-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="5b47e-211">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="5b47e-211">Positions</span></span>

<span data-ttu-id="5b47e-212">ตำแหน่งคือแต่ละอินสแตนซ์ของงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="5b47e-213">ตัวอย่างเช่น ตำแหน่ง "ผู้จัดการฝ่ายขาย (ตะวันออก)" เป็นหนึ่งในตำแหน่งที่เชื่อมโยงกับงาน "ผู้จัดการฝ่ายขาย"</span><span class="sxs-lookup"><span data-stu-id="5b47e-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="5b47e-214">ตำแหน่งมีอยู่ในแผนก</span><span class="sxs-lookup"><span data-stu-id="5b47e-214">A position exists in a department.</span></span> <span data-ttu-id="5b47e-215">สามารถเชื่อมโยงผู้ปฏิบัติงานหนึ่งรายกับแต่ละตำแหน่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="5b47e-216">เก็บข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ไว้ เมื่อคุณตั้งค่าตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="5b47e-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="5b47e-217">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-217">Position (required)</span></span>
- <span data-ttu-id="5b47e-218">คำอธิบาย (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-218">Description (required)</span></span>
- <span data-ttu-id="5b47e-219">งาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-219">Job (required)</span></span>
- <span data-ttu-id="5b47e-220">แผนก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-220">Department (required)</span></span>
- <span data-ttu-id="5b47e-221">ชนิดตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-221">Position type (required)</span></span>
- <span data-ttu-id="5b47e-222">จำนวนบุคลากรเทียบเท่าเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="5b47e-222">Full-time equivalent</span></span>
- <span data-ttu-id="5b47e-223">ชั่วโมงปกติรายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="5b47e-224">ชำระโดยนิติบุคคล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="5b47e-225">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-225">Pay cycle (required)</span></span>
- <span data-ttu-id="5b47e-226">มิติทางการเงินเริ่มต้น – ศูนย์ต้นทุน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="5b47e-227">การมอบหมายผู้ปฏิบัติงาน – ผู้ปฏิบัติงาน การเริ่มต้นการกำหนด การสิ้นสุดการกำหนด รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="5b47e-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="5b47e-228">ถ้าตำแหน่งหลายตำแหน่งในแผนกเดียวกันเกี่ยวข้องกับงานเดียวกัน จะมีการรวมลงในตำแหน่งหนึ่งๆ ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="5b47e-229">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="5b47e-230">จัดระเบียบบุคลากรของคุณโดยใช้แผนก งาน และตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="5b47e-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="5b47e-231">ตั้งค่าตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="5b47e-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="5b47e-232">แผนก</span><span class="sxs-lookup"><span data-stu-id="5b47e-232">Departments</span></span>

<span data-ttu-id="5b47e-233">แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5b47e-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="5b47e-234">แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5b47e-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="5b47e-235">คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="5b47e-236">แผนกอาจมีความรับผิดชอบกำไรและขาดทุน</span><span class="sxs-lookup"><span data-stu-id="5b47e-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="5b47e-237">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="5b47e-238">สร้างแผนกและการเชื่อมโยงกับลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="5b47e-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="5b47e-239">กำหนดฝ่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="5b47e-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="5b47e-240">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="5b47e-241">รอบการชำระค่าจ้างกำหนดความถี่ในการรันค่าจ้าง และจำนวนวันที่เจาะจงเมื่อผู้ปฏิบัติงานได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="5b47e-242">ตัวอย่างเช่น รอบการชำระค่าจ้างอาจเป็นรายเดือน และพนักงานอาจได้รับค่าจ้างในวันสุดท้ายของเดือนนั้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="5b47e-243">อีกทางหนึ่งคือ รอบการชำระค่าจ้างอาจเป็นรายสัปดาห์ และพนักงานอาจได้รับค่าจ้างในวันอังคารหลังจากจุดสิ้นสุดของรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="5b47e-244">รอบการชำระค่าจ้างถูกกำหนดให้กับตำแหน่ง เพื่อควบคุมเวลาที่ผู้ปฏิบัติงานในตำแหน่งเหล่านั้นได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="5b47e-245">หลังจากที่คุณสร้างรอบการชำระค่าจ้าง คุณสามารถสร้างรอบระยะเวลาการชำระค่าจ้างสำหรับแต่ละรอบได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="5b47e-246">รอบการชำระค่าจ้างแต่ละรอบรวมถึงวันที่ของการชำระเงินเริ่มต้นที่ยึดตามข้อมูลที่คุณให้</span><span class="sxs-lookup"><span data-stu-id="5b47e-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="5b47e-247">อย่างไรก็ตาม คุณสามารถแก้ไขวันที่การชำระเงินเริ่มต้นได้ในรอบการชำระค่าจ้างเพื่อให้อนุญาตการยกเว้น เช่น เมื่อวันที่ชำระเงินตรงกับวันหยุด</span><span class="sxs-lookup"><span data-stu-id="5b47e-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="5b47e-248">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="5b47e-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="5b47e-249">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-249">Pay cycle (required)</span></span>
- <span data-ttu-id="5b47e-250">ความถี่ของรอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="5b47e-251">วันที่เริ่มรอบระยะเวลา (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="5b47e-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="5b47e-252">วันที่การชำระเงินเริ่มต้น (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="5b47e-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="5b47e-253">ข้อมูลนี้ถูกรวมเข้ากับ Dayforce เป็นกลุ่มค่าจ้าง และจะถูกแยกตามประเทศหรือภูมิภาคสำหรับรอบการชำระค่าจ้างแต่ละรอบ</span><span class="sxs-lookup"><span data-stu-id="5b47e-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="5b47e-254">ต้องมีการสร้างรอบระยะเวลาการชำระค่าจ้างอย่างน้อยหนึ่งรายการ ก่อนที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="5b47e-255">Dayforce สร้างปฏิทินกลุ่มค่าจ้างและวันที่ในการชำระเงิน โดยยึดตามวันที่เริ่มต้นของรอบระยะเวลาการชำระค่าจ้างแรก และวันที่ชำระเงินเริ่มต้นที่ตั้งค่าใน Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="5b47e-256">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-256">Earning codes</span></span>

<span data-ttu-id="5b47e-257">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="5b47e-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5b47e-258">รหัสมีพารามิเตอร์ต่าง ๆ ที่เกี่ยวข้องกับรายได้ เช่น แต่ละ กฎทางบัญชี กฎภาษี และรายงานความต้องการและความสามารถในการรวมได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="5b47e-259">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="5b47e-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="5b47e-260">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-260">Earning Code (required)</span></span>
- <span data-ttu-id="5b47e-261">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-261">Description</span></span>
- <span data-ttu-id="5b47e-262">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="5b47e-262">Unit of measure</span></span>
- <span data-ttu-id="5b47e-263">ประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="5b47e-264">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-264">Worker data</span></span>

<span data-ttu-id="5b47e-265">เรกคอร์ดสำหรับชนิดต่างๆ ของผู้ปฏิบัติงานที่คุณมี มีความสำคัญสำหรับระบบค่าจ้างและทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="5b47e-266">ข้อมูลที่คุณป้อนสามารถใช้ติดตามผู้ปฏิบัติงานและข้อมูลส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="5b47e-267">คุณสามารถรักษาข้อมูลต่อไปนี้สำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="5b47e-268">**พื้นฐาน** – รักษาข้อมูลพื้นฐานเกี่ยวกับผู้ปฏิบัติงาน เช่น ข้อมูลการติดต่อ ข้อมูลทางประชากรศาสตร์ ข้อมูลการระบุรหัสประจำตัว ข้อมูลครอบครัว สถานะการรับราชการทหาร ข้อมูลคนต่างด้าว และผู้ติดต่อได้ในกรณีฉุกเฉินและส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="5b47e-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="5b47e-269">**การจ้างงาน** – รักษาข้อมูลเกี่ยวกับการจ้างงานของผู้ปฏิบัติงาน เช่น บริษัท หรือสังกัดองค์กร การมอบหมายตำแหน่งงาน วันที่เริ่มต้นและสิ้นสุด สิทธิการทำงาน เงื่อนไขในการจ้างงาน เงินบำนาญ วันหยุดพักผ่อน และข้อมูลการย้ายสถานที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="5b47e-270">**การลางานและการขาดงาน** – รักษาข้อมูลเกี่ยวกับการขาดงานของผู้ปฏิบัติงาน เช่น ปฏิทินการทำงาน ธุรกรรมการขาดงาน และการตั้งค่าการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="5b47e-271">**ค่าตอบแทนและค่าจ้าง** – รักษาข้อมูลเกี่ยวกับแผนค่าตอบแทนของผู้ปฏิบัติงานและข้อมูลค่าจ้าง เช่น การลงทะเบียนสำหรับแผน รางวัล ประสิทธิภาพ ค่าคอมมิชชัน ข้อมูลภาษี การเกษียณอายุ และการหักเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="5b47e-272">เมื่อคุณป้อนข้อมูลผู้ปฏิบัติงาน พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="5b47e-273">ข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="5b47e-273">General information</span></span>

- <span data-ttu-id="5b47e-274">หมายเลขบุคลากร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-274">Personnel number (required)</span></span>
- <span data-ttu-id="5b47e-275">ชื่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-275">First name (required)</span></span>
- <span data-ttu-id="5b47e-276">นามสกุล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-276">Last name (required)</span></span>
- <span data-ttu-id="5b47e-277">ชื่อกลาง</span><span class="sxs-lookup"><span data-stu-id="5b47e-277">Middle name</span></span>
- <span data-ttu-id="5b47e-278">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-278">Seniority date</span></span>
- <span data-ttu-id="5b47e-279">เรียกว่า</span><span class="sxs-lookup"><span data-stu-id="5b47e-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="5b47e-280">ข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="5b47e-280">Personal information</span></span>

- <span data-ttu-id="5b47e-281">สถานภาพการสมรส (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-281">Marital status (required)</span></span>
- <span data-ttu-id="5b47e-282">วันที่เกิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-282">Birth date (required)</span></span>
- <span data-ttu-id="5b47e-283">เพศ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-283">Gender (required)</span></span>
- <span data-ttu-id="5b47e-284">บุคคลทุพพลภาพ</span><span class="sxs-lookup"><span data-stu-id="5b47e-284">Person with disabilities</span></span>
- <span data-ttu-id="5b47e-285">สัญชาติประเทศภูมิภาค (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="5b47e-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="5b47e-286">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="5b47e-286">Address information</span></span>

- <span data-ttu-id="5b47e-287">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-287">Primary (required)</span></span>
- <span data-ttu-id="5b47e-288">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-288">Country/region (required)</span></span>
- <span data-ttu-id="5b47e-289">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-289">Postal code (required)</span></span>
- <span data-ttu-id="5b47e-290">หมายเลขถนน (จำเป็น) (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="5b47e-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="5b47e-291">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="5b47e-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="5b47e-292">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-292">City (required)</span></span>
- <span data-ttu-id="5b47e-293">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-293">State (required)</span></span>
- <span data-ttu-id="5b47e-294">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="5b47e-295">ข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="5b47e-295">Contact information</span></span> 

- <span data-ttu-id="5b47e-296">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-296">Primary (required)</span></span>
- <span data-ttu-id="5b47e-297">หมายเลขผู้ติดต่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-297">Contact number (required)</span></span>
- <span data-ttu-id="5b47e-298">การขยาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="5b47e-299">ข้อมูลค่าจ้างและรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-299">Payroll information and earning codes</span></span>

<span data-ttu-id="5b47e-300">พนักงานอาจถูกกำหนดรายได้เฉพาะที่ความถี่ที่กำหนดของการชำระเงิน และมีวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="5b47e-301">ฟิลด์ต่อไปนี้จะใช้ใน Dayforce เพื่อช่วยในการรับประกันว่า การกำหนดลักษณะและการตั้งค่าเหล่านั้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="5b47e-302">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-302">Earning codes</span></span>

- <span data-ttu-id="5b47e-303">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-303">Position (required)</span></span>
- <span data-ttu-id="5b47e-304">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-304">Earning Code (required)</span></span>
- <span data-ttu-id="5b47e-305">ความถี่ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-305">Frequency (required)</span></span>
- <span data-ttu-id="5b47e-306">จำนวน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="5b47e-307">ข้อมูลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-307">Payroll information</span></span>

- <span data-ttu-id="5b47e-308">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="5b47e-308">Payment Method</span></span>
- <span data-ttu-id="5b47e-309">ภูมิภาคเศรษฐกิจ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-309">Economic Region (required)</span></span>
- <span data-ttu-id="5b47e-310">รหัสสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-310">Employee Benefits ID</span></span>
- <span data-ttu-id="5b47e-311">หมายเลขรหัสประจำชาติ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-311">National ID Number (required)</span></span>
- <span data-ttu-id="5b47e-312">หมายเลขการรับราชการทหาร</span><span class="sxs-lookup"><span data-stu-id="5b47e-312">Military Service Number</span></span>
- <span data-ttu-id="5b47e-313">รหัสกะ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-313">Shift ID (required)</span></span>
- <span data-ttu-id="5b47e-314">หมายเลขภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-314">Tax Number (required)</span></span>
- <span data-ttu-id="5b47e-315">รหัสสหภาพ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-315">Union ID (required)</span></span>
- <span data-ttu-id="5b47e-316">รหัสวันทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-316">Work Day ID (required)</span></span>
- <span data-ttu-id="5b47e-317">หมายเลขใบอนุญาตทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="5b47e-318">สำหรับวิธีการชำระเงิน เม็กซิโกสนับสนุน **เงินสด** **เช็ค** (เช็คจริงของบริษัท) และ **การชำระเงินทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="5b47e-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="5b47e-319">ถ้าไม่มีการระบุวิธีการชำระเงิน **เช็ค** จะถูกใช้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="5b47e-320">รายละเอียดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-320">Employment details</span></span>

<span data-ttu-id="5b47e-321">ประวัติรายละเอียดตการจ้างงานถูกใช้เป็นข้อมูลสำคัญในการสืบทอดการพนักงานจ้างงานของพนักงาน การหยุดชะงัก และสถานะการจ้างงานใหม่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="5b47e-322">Dayforce สนับสนุนเรกคอร์ดการจ้างงานที่ใช้งานอยู่เพียงรายการเดียวในแต่ละครั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="5b47e-323">วันที่เริ่มต้นการจ้างงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-323">Employment start date (required)</span></span>
- <span data-ttu-id="5b47e-324">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-324">Employment end date</span></span>
- <span data-ttu-id="5b47e-325">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-325">Start date</span></span>
- <span data-ttu-id="5b47e-326">วันที่เริ่มต้นที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="5b47e-326">Adjusted start date</span></span>
- <span data-ttu-id="5b47e-327">วันที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="5b47e-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="5b47e-328">เหตุผลที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="5b47e-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="5b47e-329">วันสำคัญของพนักงานได้รับมาโดยใช้ข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5b47e-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="5b47e-330">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-330">Talent</span></span>                | <span data-ttu-id="5b47e-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b47e-332">วันที่จ้างงานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5b47e-332">Most recent hire date</span></span> | <span data-ttu-id="5b47e-333">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="5b47e-334">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-334">Termination date</span></span>      | <span data-ttu-id="5b47e-335">วันที่สิ้นสุดการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="5b47e-336">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-336">Start date</span></span>            | <span data-ttu-id="5b47e-337">วันที่เริ่มต้นที่ปรับปรุงแล้ว วันที่เริ่มต้น หรือการเริ่มต้นการจ้างงานของเรกคอร์ประวัติการจ้างงานที่ไม่ได้ใช้งานอยู่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="5b47e-338">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="5b47e-338">Original hire date</span></span>    | <span data-ttu-id="5b47e-339">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานแรกสุด</span><span class="sxs-lookup"><span data-stu-id="5b47e-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="5b47e-340">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-340">Compensation</span></span>

<span data-ttu-id="5b47e-341">แผนค่าตอบแทนคงต้องเชื่อมโยงกับตำแหน่งหลักของพนักงานทุกตำแหน่ง ตลอดรอบระยะเวลาการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="5b47e-342">รอบระยะเวลานี้เริ่มต้นในวันที่ที่พนักงานถูกจ้างงาน (หรือวันที่เริ่มต้นการจ้างงาน) และดำเนินต่อไปจนกว่าจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="5b47e-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="5b47e-343">วันที่มีผลบังคับใช้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-343">Effective Date (required)</span></span>
- <span data-ttu-id="5b47e-344">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="5b47e-344">Expiration date</span></span>
- <span data-ttu-id="5b47e-345">อัตราการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-345">Pay Rate (required)</span></span>
- <span data-ttu-id="5b47e-346">การแปลงอัตราค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="5b47e-347">จำนวนเทียบเท่ารายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="5b47e-348">จำนวนเทียบเท่ารายชั่วโมง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="5b47e-349">ถ้าพนักงานรายชั่วโมงมีตำแหน่งหลายตำแหน่ง ค่าตอบแทนคงที่ของตำแหน่งหลักจะถูกนำเข้าใน Dayforce เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="5b47e-350">สำหรับตำแหน่งที่ไม่ใช่ตำแหน่งหลัก อัตรารายชั่วโมงถูกบันทึกลงในตำแหน่งที่สอดคล้องกันใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="5b47e-351">ถ้าพนักงานประจำมีตำแหน่งหลายตำแหน่ง จะได้รับอัตราชั่วโมงสะสมและเงินเดือนต่อปีระหว่างตำแหน่งที่ใช้งานอยู่ทั้งหมด และถูกใช้เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="5b47e-352">หมายเลขรหัส</span><span class="sxs-lookup"><span data-stu-id="5b47e-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="5b47e-353">ตัวระบุประกันสังคม</span><span class="sxs-lookup"><span data-stu-id="5b47e-353">Social Security identifier</span></span> 

<span data-ttu-id="5b47e-354">พนักงานทุกคนต้องมีตัวระบุหลักหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="5b47e-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="5b47e-355">ตัวระบุนี้ต้องเป็นชนิดรหัส **SSN**</span><span class="sxs-lookup"><span data-stu-id="5b47e-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="5b47e-356">ใน Dayforce จะได้รับมาโดยอัตโนมัติเป็นตัวระบุประกันสังคมของพนักงานที่จำเป็นสำหรับการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="5b47e-357">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-357">Primary (required)</span></span>
- <span data-ttu-id="5b47e-358">ชนิดข้อมูลประจำตัว = "SSN"</span><span class="sxs-lookup"><span data-stu-id="5b47e-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="5b47e-359">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="5b47e-359">Issued Date</span></span>
- <span data-ttu-id="5b47e-360">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="5b47e-360">Expiration Date</span></span>

<span data-ttu-id="5b47e-361">พนักงานสามารถประกาศหมายเลขการระบุรหัสประจำตัวหลายเลขของชนิดการระบุรหัสประจำตัว **SSN**</span><span class="sxs-lookup"><span data-stu-id="5b47e-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="5b47e-362">อย่างไรก็ตาม เฉพาะเรกคอร์ดที่ถูกทำเครื่องหมายเป็น **หลัก** ถูกรวมเข้ากับ Dayforce ไม่ว่าหมายเลขจะใช้งานอยู่ หรือหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="5b47e-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="5b47e-363">บัญชีธนาคารและการเบิกจ่าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="5b47e-364">ต้องป้อนข้อมูลบัญชีธนาคารที่ถูกต้องสำหรับพนักงานใดๆ ที่เลือกที่จะรับการชำระเงินผ่านการโอนย้ายของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="5b47e-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="5b47e-365">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-365">Talent</span></span>                         | <span data-ttu-id="5b47e-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b47e-367">หมายเลขบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="5b47e-368">รหัส SWIFT (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-368">SWIFT code (required)</span></span>          | <span data-ttu-id="5b47e-369">ฟิลด์ **รหัสธนาคาร** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="5b47e-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="5b47e-370">หมายเลขสาขา (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="5b47e-371">ชนิดของบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-371">Bank account type (required)</span></span>   | <span data-ttu-id="5b47e-372">ฟิลด์ **ชนิดของบัญชี** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="5b47e-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="5b47e-373">ค่าที่ได้รับการสนับสนุนได้แก่ **การตรวจสอบ** และ **ค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="5b47e-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="5b47e-374">พนักงานที่เลือกจะรับการชำระผ่านการโอนผ่านบัญชีธนาคาร ต้องมีลิงก์ไปยังบัญชีเงินส่วนที่เหลือที่อยู่ภายใต้นิติบุคคลที่มีที่อยู่หลักในเม็กซิโก และเชื่อมโยงกับบัญชีธนาคารที่ถูกต้องจากธนาคารเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="5b47e-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="5b47e-375">บัญชีที่ไม่ใช่เงินส่วนที่เหลืออื่นๆ ทั้งหมดจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="5b47e-376">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="5b47e-376">Address information</span></span>

<span data-ttu-id="5b47e-377">พนักงานทุกคนต้องมีสถานที่หลักหนึ่งแห่ง</span><span class="sxs-lookup"><span data-stu-id="5b47e-377">Every employee must have one primary location.</span></span> <span data-ttu-id="5b47e-378">ใน Dayforce สถานที่นี้จะใช้เพื่อกำหนดที่พักอาศัยหลักของพนักงานสำหรับวัตถุประสงค์ด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="5b47e-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="5b47e-379">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-379">Primary (required)</span></span>
- <span data-ttu-id="5b47e-380">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-380">Country/region (required)</span></span>
- <span data-ttu-id="5b47e-381">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="5b47e-382">ถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-382">Street (required)</span></span>
- <span data-ttu-id="5b47e-383">หมายเลขถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-383">Street Number (required)</span></span>
- <span data-ttu-id="5b47e-384">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="5b47e-384">Building Complement</span></span>
- <span data-ttu-id="5b47e-385">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-385">City (required)</span></span>
- <span data-ttu-id="5b47e-386">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-386">State (required)</span></span>
- <span data-ttu-id="5b47e-387">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="5b47e-388">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="5b47e-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="5b47e-389">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในสหรัฐอเมริกาและแคนาดา ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="5b47e-390">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-390">Departments are required on positions.</span></span>
- <span data-ttu-id="5b47e-391">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="5b47e-392">คุณสามารถตั้งค่าคอนฟิก Talent เพื่อกำหนดว่า ตำแหน่งต้องระบุแผนก</span><span class="sxs-lookup"><span data-stu-id="5b47e-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="5b47e-393">เมื่อต้องการทำเช่นนี้ ไปยัง **ตำแหน่งที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล > ตำแหน่ง > ต้องการแผนกในตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="5b47e-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="5b47e-394">เราขอแนะนำให้ การตั้งค่านี้ถูกบังคับใช้สำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="5b47e-395">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-395">Job types</span></span>

<span data-ttu-id="5b47e-396">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="5b47e-397">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="5b47e-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="5b47e-398">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5b47e-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="5b47e-399">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="5b47e-400">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-401">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-401">Job type</span></span>   | <span data-ttu-id="5b47e-402">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="5b47e-403">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5b47e-403">Hourly</span></span>     | <span data-ttu-id="5b47e-404">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5b47e-404">Hourly</span></span>      |
| <span data-ttu-id="5b47e-405">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-405">Salaried</span></span>   | <span data-ttu-id="5b47e-406">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="5b47e-407">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-407">Position types</span></span> 

<span data-ttu-id="5b47e-408">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="5b47e-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="5b47e-409">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b47e-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="5b47e-410">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-411">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="5b47e-411">Position type</span></span>   | <span data-ttu-id="5b47e-412">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="5b47e-413">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="5b47e-413">Full-time</span></span>       | <span data-ttu-id="5b47e-414">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="5b47e-414">Full time employee</span></span> |
| <span data-ttu-id="5b47e-415">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b47e-415">Part-time</span></span>       | <span data-ttu-id="5b47e-416">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b47e-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="5b47e-417">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="5b47e-417">Reason codes</span></span>

<span data-ttu-id="5b47e-418">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="5b47e-419">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="5b47e-420">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-421">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="5b47e-421">Reason code</span></span>    | <span data-ttu-id="5b47e-422">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-422">Description</span></span>      | <span data-ttu-id="5b47e-423">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="5b47e-424">การลาออก</span><span class="sxs-lookup"><span data-stu-id="5b47e-424">RESIGNATION</span></span>    | <span data-ttu-id="5b47e-425">การลาออก</span><span class="sxs-lookup"><span data-stu-id="5b47e-425">Resignation</span></span>      | <span data-ttu-id="5b47e-426">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-426">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-427">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-427">TERMINATION</span></span>    | <span data-ttu-id="5b47e-428">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-428">Termination</span></span>      | <span data-ttu-id="5b47e-429">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-429">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-430">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-430">RETIREMENT</span></span>     | <span data-ttu-id="5b47e-431">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-431">Retirement</span></span>       | <span data-ttu-id="5b47e-432">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-432">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-433">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-433">OTHER</span></span>          | <span data-ttu-id="5b47e-434">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-434">Other Reasons</span></span>    | <span data-ttu-id="5b47e-435">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-435">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-436">ความตาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-436">DEATH</span></span>          | <span data-ttu-id="5b47e-437">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="5b47e-437">Death</span></span>            | <span data-ttu-id="5b47e-438">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-438">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="5b47e-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="5b47e-440">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="5b47e-440">Leave of Absence</span></span> | <span data-ttu-id="5b47e-441">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-441">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="5b47e-442">CONTRACTEND</span></span>    | <span data-ttu-id="5b47e-443">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="5b47e-443">End of Contract</span></span>  | <span data-ttu-id="5b47e-444">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-444">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="5b47e-445">SALARYCHANGE</span></span>   | <span data-ttu-id="5b47e-446">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-446">Change of Salary</span></span> | <span data-ttu-id="5b47e-447">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="5b47e-448">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="5b47e-448">Marital status</span></span>

<span data-ttu-id="5b47e-449">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5b47e-450">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="5b47e-451">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-451">Talent</span></span>                 | <span data-ttu-id="5b47e-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="5b47e-453">สมรส</span><span class="sxs-lookup"><span data-stu-id="5b47e-453">Married</span></span>                | <span data-ttu-id="5b47e-454">สมรส</span><span class="sxs-lookup"><span data-stu-id="5b47e-454">Married</span></span>              |
| <span data-ttu-id="5b47e-455">โสด</span><span class="sxs-lookup"><span data-stu-id="5b47e-455">Single</span></span>                 | <span data-ttu-id="5b47e-456">โสด</span><span class="sxs-lookup"><span data-stu-id="5b47e-456">Single</span></span>               |
| <span data-ttu-id="5b47e-457">หม้าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-457">Widowed</span></span>                | <span data-ttu-id="5b47e-458">หม้าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-458">Widowed</span></span>              |
| <span data-ttu-id="5b47e-459">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-459">Divorced</span></span>               | <span data-ttu-id="5b47e-460">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-460">Divorced</span></span>             |
| <span data-ttu-id="5b47e-461">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="5b47e-461">Registered Partnership</span></span> | <span data-ttu-id="5b47e-462">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="5b47e-462">Domestic Partnership</span></span> |
| <span data-ttu-id="5b47e-463">None</span><span class="sxs-lookup"><span data-stu-id="5b47e-463">None</span></span>                   | <span data-ttu-id="5b47e-464">None</span><span class="sxs-lookup"><span data-stu-id="5b47e-464">None</span></span>                 |
| <span data-ttu-id="5b47e-465">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-465">Cohabiting</span></span>             | <span data-ttu-id="5b47e-466">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="5b47e-467">เพศ</span><span class="sxs-lookup"><span data-stu-id="5b47e-467">Gender</span></span>

<span data-ttu-id="5b47e-468">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5b47e-469">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="5b47e-470">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-470">Talent</span></span>       | <span data-ttu-id="5b47e-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="5b47e-472">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-472">Male</span></span>         | <span data-ttu-id="5b47e-473">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-473">Male</span></span>            |
| <span data-ttu-id="5b47e-474">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="5b47e-474">Female</span></span>       | <span data-ttu-id="5b47e-475">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="5b47e-475">Female</span></span>          |
| <span data-ttu-id="5b47e-476">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="5b47e-476">Non-specific</span></span> | <span data-ttu-id="5b47e-477">*ไม่สนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="5b47e-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="5b47e-478">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-478">Earning codes</span></span>

<span data-ttu-id="5b47e-479">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="5b47e-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5b47e-480">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5b47e-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="5b47e-481">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="5b47e-482">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5b47e-482">Supported frequencies</span></span>

- <span data-ttu-id="5b47e-483">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5b47e-483">All</span></span>
- <span data-ttu-id="5b47e-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="5b47e-484">EVERYPAY</span></span>
- <span data-ttu-id="5b47e-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="5b47e-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="5b47e-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="5b47e-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="5b47e-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="5b47e-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="5b47e-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-488">1OFMTH</span></span>
- <span data-ttu-id="5b47e-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-489">LASTOFMTH</span></span>
- <span data-ttu-id="5b47e-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-490">2OFMTH</span></span>
- <span data-ttu-id="5b47e-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-491">3OFMTH</span></span>
- <span data-ttu-id="5b47e-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-492">4OFMTH</span></span>
- <span data-ttu-id="5b47e-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-493">5OFMTH</span></span>
- <span data-ttu-id="5b47e-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-494">1N2OFMTH</span></span>
- <span data-ttu-id="5b47e-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-495">3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-496">1N3OFMTH</span></span>
- <span data-ttu-id="5b47e-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-497">1N4OFMTH</span></span>
- <span data-ttu-id="5b47e-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-498">2N3OFMTH</span></span>
- <span data-ttu-id="5b47e-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-499">2N4OFMTH</span></span>
- <span data-ttu-id="5b47e-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="5b47e-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="5b47e-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="5b47e-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="5b47e-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="5b47e-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="5b47e-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="5b47e-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="5b47e-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="5b47e-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="5b47e-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="5b47e-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="5b47e-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5b47e-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="5b47e-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5b47e-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="5b47e-512">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="5b47e-512">Addresses</span></span>

<span data-ttu-id="5b47e-513">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="5b47e-514">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="5b47e-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="5b47e-515">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-515">Talent</span></span>          | <span data-ttu-id="5b47e-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="5b47e-517">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="5b47e-517">Country/Region</span></span>  | <span data-ttu-id="5b47e-518">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="5b47e-518">Country Code</span></span>          |
| <span data-ttu-id="5b47e-519">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="5b47e-519">Zip/Postal Code</span></span> | <span data-ttu-id="5b47e-520">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="5b47e-520">Postal Code</span></span>           |
| <span data-ttu-id="5b47e-521">สถานะ</span><span class="sxs-lookup"><span data-stu-id="5b47e-521">State</span></span>           | <span data-ttu-id="5b47e-522">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="5b47e-522">State Code</span></span>            |
| <span data-ttu-id="5b47e-523">เมือง</span><span class="sxs-lookup"><span data-stu-id="5b47e-523">City</span></span>            | <span data-ttu-id="5b47e-524">เมือง</span><span class="sxs-lookup"><span data-stu-id="5b47e-524">City</span></span>                  |
| <span data-ttu-id="5b47e-525">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="5b47e-525">County</span></span>          | <span data-ttu-id="5b47e-526">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="5b47e-526">County (Municipality)</span></span> |
| <span data-ttu-id="5b47e-527">ถนน</span><span class="sxs-lookup"><span data-stu-id="5b47e-527">Street</span></span>          | <span data-ttu-id="5b47e-528">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="5b47e-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="5b47e-529">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="5b47e-529">Tax regions</span></span>

<span data-ttu-id="5b47e-530">ภูมิภาคการเก็บภาษีถูกใช้เพื่อกำหนดภาษีที่เหมาะสมที่ควรนำมาใช้ในระหว่างการสร้างระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="5b47e-531">ภูมิภาคการเก็บภาษีถูกแม็ปไปยัง Dayforce เป็นที่อยู่ของสถานที่</span><span class="sxs-lookup"><span data-stu-id="5b47e-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="5b47e-532">ภูมิภาคการเก็บภาษีเริ่มต้นต้องเชื่อมโยงกับตำแหน่งงานที่ใช้งานอยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="5b47e-533">ภูมิภาคการเก็บภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-533">Tax region (required)</span></span>
- <span data-ttu-id="5b47e-534">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-534">Country/Region (required)</span></span>
- <span data-ttu-id="5b47e-535">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-535">State (required)</span></span>
- <span data-ttu-id="5b47e-536">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="5b47e-536">County</span></span> 
- <span data-ttu-id="5b47e-537">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="5b47e-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="5b47e-538">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="5b47e-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="5b47e-539">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในเม็กซิโก ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5b47e-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="5b47e-540">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-540">Departments are required on positions.</span></span>
- <span data-ttu-id="5b47e-541">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5b47e-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="5b47e-542">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-542">Job types</span></span>

<span data-ttu-id="5b47e-543">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="5b47e-544">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="5b47e-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="5b47e-545">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5b47e-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="5b47e-546">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="5b47e-547">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-548">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-548">Job type</span></span>   | <span data-ttu-id="5b47e-549">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="5b47e-550">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5b47e-550">Hourly</span></span>     | <span data-ttu-id="5b47e-551">MX รายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5b47e-551">MX Hourly</span></span>   |
| <span data-ttu-id="5b47e-552">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-552">Salaried</span></span>   | <span data-ttu-id="5b47e-553">MX รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="5b47e-554">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-554">Position types</span></span> 

<span data-ttu-id="5b47e-555">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="5b47e-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="5b47e-556">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b47e-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="5b47e-557">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-558">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="5b47e-558">Position type</span></span>   | <span data-ttu-id="5b47e-559">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="5b47e-560">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="5b47e-560">Full-time</span></span>       | <span data-ttu-id="5b47e-561">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="5b47e-561">Full time employee</span></span> |
| <span data-ttu-id="5b47e-562">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b47e-562">Part-time</span></span>       | <span data-ttu-id="5b47e-563">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="5b47e-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="5b47e-564">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="5b47e-564">Reason codes</span></span>

<span data-ttu-id="5b47e-565">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="5b47e-566">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="5b47e-567">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-568">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="5b47e-568">Reason code</span></span>            | <span data-ttu-id="5b47e-569">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-569">Description</span></span>                    | <span data-ttu-id="5b47e-570">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="5b47e-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="5b47e-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="5b47e-572">การออกก่อนค่าจ้างแรก</span><span class="sxs-lookup"><span data-stu-id="5b47e-572">Departure before first payroll</span></span> | <span data-ttu-id="5b47e-573">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-573">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-574">การลาออก</span><span class="sxs-lookup"><span data-stu-id="5b47e-574">RESIGNATION</span></span>            | <span data-ttu-id="5b47e-575">การลาออก</span><span class="sxs-lookup"><span data-stu-id="5b47e-575">Resignation</span></span>                    | <span data-ttu-id="5b47e-576">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-576">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-577">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="5b47e-577">PENSION</span></span>                | <span data-ttu-id="5b47e-578">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="5b47e-578">Pension</span></span>                        | <span data-ttu-id="5b47e-579">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-579">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-580">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-580">TERMINATION</span></span>            | <span data-ttu-id="5b47e-581">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-581">Termination</span></span>                    | <span data-ttu-id="5b47e-582">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-582">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-583">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-583">RETIREMENT</span></span>             | <span data-ttu-id="5b47e-584">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-584">Retirement</span></span>                     | <span data-ttu-id="5b47e-585">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-585">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-586">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-586">ABSENTEE</span></span>               | <span data-ttu-id="5b47e-587">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-587">Absentee</span></span>                       | <span data-ttu-id="5b47e-588">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-588">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-589">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-589">OTHER</span></span>                  | <span data-ttu-id="5b47e-590">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-590">Other Reasons</span></span>                  | <span data-ttu-id="5b47e-591">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-591">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-592">การปิด</span><span class="sxs-lookup"><span data-stu-id="5b47e-592">CLOSURE</span></span>                | <span data-ttu-id="5b47e-593">การปิดของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="5b47e-593">Business Closure</span></span>               | <span data-ttu-id="5b47e-594">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-594">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-595">ความตาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-595">DEATH</span></span>                  | <span data-ttu-id="5b47e-596">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="5b47e-596">Death</span></span>                          | <span data-ttu-id="5b47e-597">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-597">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="5b47e-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="5b47e-599">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="5b47e-599">Leave of Absence</span></span>               | <span data-ttu-id="5b47e-600">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-600">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="5b47e-601">CONTRACTEND</span></span>            | <span data-ttu-id="5b47e-602">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="5b47e-602">End of Contract</span></span>                | <span data-ttu-id="5b47e-603">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-603">Terminate worker</span></span>     |
| <span data-ttu-id="5b47e-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="5b47e-604">SALARYCHANGE</span></span>           | <span data-ttu-id="5b47e-605">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5b47e-605">Change of Salary</span></span>               | <span data-ttu-id="5b47e-606">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="5b47e-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="5b47e-607">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-607">Terms of employment</span></span>

<span data-ttu-id="5b47e-608">มีการใช้เงื่อนไขของการจ้างงาน เพื่อสร้างประเภทและตัวอย่างของการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="5b47e-609">เงื่อนไขถูกแม็ปกับ Dayforce เป็นค่าตัวบ่งชี้การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="5b47e-610">เงื่อนไขการจ้างงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="5b47e-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="5b47e-611">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-611">Terms of employment</span></span>   | <span data-ttu-id="5b47e-612">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="5b47e-613">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="5b47e-613">Regular</span></span>               | <span data-ttu-id="5b47e-614">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="5b47e-614">Regular</span></span>     |
| <span data-ttu-id="5b47e-615">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="5b47e-615">Direct</span></span>                | <span data-ttu-id="5b47e-616">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="5b47e-616">Direct</span></span>      |
| <span data-ttu-id="5b47e-617">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-617">Internship</span></span>            | <span data-ttu-id="5b47e-618">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-618">Internship</span></span>  |
| <span data-ttu-id="5b47e-619">ถาวร</span><span class="sxs-lookup"><span data-stu-id="5b47e-619">Permanent</span></span>             | <span data-ttu-id="5b47e-620">ถาวร</span><span class="sxs-lookup"><span data-stu-id="5b47e-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="5b47e-621">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="5b47e-621">Marital status</span></span>

<span data-ttu-id="5b47e-622">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5b47e-623">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="5b47e-624">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-624">Talent</span></span>                 | <span data-ttu-id="5b47e-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="5b47e-626">สมรส</span><span class="sxs-lookup"><span data-stu-id="5b47e-626">Married</span></span>                | <span data-ttu-id="5b47e-627">สมรส</span><span class="sxs-lookup"><span data-stu-id="5b47e-627">Married</span></span>                   |
| <span data-ttu-id="5b47e-628">โสด</span><span class="sxs-lookup"><span data-stu-id="5b47e-628">Single</span></span>                 | <span data-ttu-id="5b47e-629">โสด</span><span class="sxs-lookup"><span data-stu-id="5b47e-629">Single</span></span>                    |
| <span data-ttu-id="5b47e-630">หม้าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-630">Widowed</span></span>                | <span data-ttu-id="5b47e-631">หม้าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-631">Widowed</span></span>                   |
| <span data-ttu-id="5b47e-632">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-632">Divorced</span></span>               | <span data-ttu-id="5b47e-633">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-633">Divorced</span></span>                  |
| <span data-ttu-id="5b47e-634">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="5b47e-634">Registered Partnership</span></span> | <span data-ttu-id="5b47e-635">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="5b47e-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="5b47e-636">None</span><span class="sxs-lookup"><span data-stu-id="5b47e-636">None</span></span>                   | <span data-ttu-id="5b47e-637">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5b47e-638">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-638">Cohabiting</span></span>             | <span data-ttu-id="5b47e-639">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="5b47e-640">เพศ</span><span class="sxs-lookup"><span data-stu-id="5b47e-640">Gender</span></span>

<span data-ttu-id="5b47e-641">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5b47e-642">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="5b47e-643">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-643">Talent</span></span>       | <span data-ttu-id="5b47e-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="5b47e-645">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-645">Male</span></span>         | <span data-ttu-id="5b47e-646">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="5b47e-646">Male</span></span>                      |
| <span data-ttu-id="5b47e-647">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="5b47e-647">Female</span></span>       | <span data-ttu-id="5b47e-648">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="5b47e-648">Female</span></span>                    |
| <span data-ttu-id="5b47e-649">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="5b47e-649">Non-specific</span></span> | <span data-ttu-id="5b47e-650">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="5b47e-651">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="5b47e-651">Payment method</span></span>

<span data-ttu-id="5b47e-652">วิธีการชำระเงินให้พนักงานและบริษัทมีวิธีในการอธิบายวิธีการจ่ายเงินแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="5b47e-653">วิธีการชำระเงินถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5b47e-654">ตารางต่อไปนี้แสดงวิธีการแม็ปวิธีการชำระเงินกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="5b47e-655">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-655">Talent</span></span>             | <span data-ttu-id="5b47e-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="5b47e-657">เงินสด</span><span class="sxs-lookup"><span data-stu-id="5b47e-657">Cash</span></span>               | <span data-ttu-id="5b47e-658">เงินสด</span><span class="sxs-lookup"><span data-stu-id="5b47e-658">Cash</span></span>                      |
| <span data-ttu-id="5b47e-659">การชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5b47e-659">Electronic Payment</span></span> | <span data-ttu-id="5b47e-660">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-660">Transfer</span></span>                  |
| <span data-ttu-id="5b47e-661">ตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="5b47e-661">Check</span></span>              | <span data-ttu-id="5b47e-662">เช็ค</span><span class="sxs-lookup"><span data-stu-id="5b47e-662">Cheque</span></span>                    |
| <span data-ttu-id="5b47e-663">ตั๋วแลกเงินธนาคาร</span><span class="sxs-lookup"><span data-stu-id="5b47e-663">Bank Draft</span></span>         | <span data-ttu-id="5b47e-664">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5b47e-665">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5b47e-665">Other</span></span>              | <span data-ttu-id="5b47e-666">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="5b47e-667">ชนิดของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="5b47e-667">Bank account type</span></span>

<span data-ttu-id="5b47e-668">ชนิดของบัญชีธนาคารถูกใช้สำหรับการชำระเงินทางอิเล็กทรอนิกส์แก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="5b47e-669">ชนิดบัญชีธนาคารถูกแม็ปกับ Dayforce เป็นข้อมูลบัญชีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="5b47e-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="5b47e-670">ชนิดของบัญชีธนาคารจะถูกแปล ตามความเหมาะสม กับค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="5b47e-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="5b47e-671">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-671">Talent</span></span>            | <span data-ttu-id="5b47e-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="5b47e-673">บัญชีกระแสรายวัน</span><span class="sxs-lookup"><span data-stu-id="5b47e-673">Checking Account</span></span>  | <span data-ttu-id="5b47e-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="5b47e-674">CheckingAccount</span></span>           |
| <span data-ttu-id="5b47e-675">บัญชีเครดิตค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5b47e-675">Payroll Account</span></span>   | <span data-ttu-id="5b47e-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="5b47e-676">PayrollAccount</span></span>            |
| <span data-ttu-id="5b47e-677">บัญชีออมทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5b47e-677">Savings Account</span></span>   | <span data-ttu-id="5b47e-678">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5b47e-679">บัญชี BankGirot</span><span class="sxs-lookup"><span data-stu-id="5b47e-679">BankGirot account</span></span> | <span data-ttu-id="5b47e-680">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5b47e-681">บัญชี PlusGirot</span><span class="sxs-lookup"><span data-stu-id="5b47e-681">PlusGirot account</span></span> | <span data-ttu-id="5b47e-682">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="5b47e-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="5b47e-683">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-683">Earning codes</span></span>

<span data-ttu-id="5b47e-684">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="5b47e-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5b47e-685">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5b47e-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="5b47e-686">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="5b47e-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="5b47e-687">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5b47e-687">Supported frequencies</span></span>

- <span data-ttu-id="5b47e-688">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5b47e-688">All</span></span>
- <span data-ttu-id="5b47e-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="5b47e-689">EVERYPAY</span></span>
- <span data-ttu-id="5b47e-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="5b47e-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="5b47e-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="5b47e-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="5b47e-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="5b47e-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="5b47e-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-693">1OFMTH</span></span>
- <span data-ttu-id="5b47e-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-694">LASTOFMTH</span></span>
- <span data-ttu-id="5b47e-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-695">2OFMTH</span></span>
- <span data-ttu-id="5b47e-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-696">3OFMTH</span></span>
- <span data-ttu-id="5b47e-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-697">4OFMTH</span></span>
- <span data-ttu-id="5b47e-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-698">5OFMTH</span></span>
- <span data-ttu-id="5b47e-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-699">1N2OFMTH</span></span>
- <span data-ttu-id="5b47e-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-700">3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-701">1N3OFMTH</span></span>
- <span data-ttu-id="5b47e-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-702">1N4OFMTH</span></span>
- <span data-ttu-id="5b47e-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-703">2N3OFMTH</span></span>
- <span data-ttu-id="5b47e-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-704">2N4OFMTH</span></span>
- <span data-ttu-id="5b47e-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="5b47e-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="5b47e-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5b47e-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="5b47e-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="5b47e-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="5b47e-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="5b47e-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="5b47e-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="5b47e-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="5b47e-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="5b47e-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="5b47e-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="5b47e-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="5b47e-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5b47e-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="5b47e-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5b47e-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="5b47e-717">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="5b47e-717">Addresses</span></span>

<span data-ttu-id="5b47e-718">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="5b47e-719">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="5b47e-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="5b47e-720">Talent</span><span class="sxs-lookup"><span data-stu-id="5b47e-720">Talent</span></span>              | <span data-ttu-id="5b47e-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="5b47e-722">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="5b47e-722">Country/Region</span></span>      | <span data-ttu-id="5b47e-723">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="5b47e-723">Country Code</span></span>          |
| <span data-ttu-id="5b47e-724">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="5b47e-724">Zip/Postal Code</span></span>     | <span data-ttu-id="5b47e-725">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="5b47e-725">Postal Code</span></span>           |
| <span data-ttu-id="5b47e-726">สถานะ</span><span class="sxs-lookup"><span data-stu-id="5b47e-726">State</span></span>               | <span data-ttu-id="5b47e-727">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="5b47e-727">State Code</span></span>            |
| <span data-ttu-id="5b47e-728">เมือง</span><span class="sxs-lookup"><span data-stu-id="5b47e-728">City</span></span>                | <span data-ttu-id="5b47e-729">เมือง</span><span class="sxs-lookup"><span data-stu-id="5b47e-729">City</span></span>                  |
| <span data-ttu-id="5b47e-730">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="5b47e-730">County</span></span>              | <span data-ttu-id="5b47e-731">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="5b47e-731">County (Municipality)</span></span> |
| <span data-ttu-id="5b47e-732">ถนน</span><span class="sxs-lookup"><span data-stu-id="5b47e-732">Street</span></span>              | <span data-ttu-id="5b47e-733">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="5b47e-733">Address Line 1</span></span>        |
| <span data-ttu-id="5b47e-734">หมายเลขถนน</span><span class="sxs-lookup"><span data-stu-id="5b47e-734">Street Number</span></span>       | <span data-ttu-id="5b47e-735">ที่อยู่ บรรทัดที่ 2</span><span class="sxs-lookup"><span data-stu-id="5b47e-735">Address Line 2</span></span>        |
| <span data-ttu-id="5b47e-736">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="5b47e-736">Building Complement</span></span> | <span data-ttu-id="5b47e-737">ที่อยู่ บรรทัดที่ 5</span><span class="sxs-lookup"><span data-stu-id="5b47e-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="5b47e-738">หมายเลขหนังสือเดินทาง</span><span class="sxs-lookup"><span data-stu-id="5b47e-738">Passport number</span></span>

<span data-ttu-id="5b47e-739">พนักงานสามารถประกาศข้อมูลหนังสือเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="5b47e-739">Employees can declare passport information.</span></span> <span data-ttu-id="5b47e-740">ข้อมูลนี้เป็นชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง** และถูกรวมอยู่ใน Dayforce เป็นส่วนหนึ่งของข้อมูลเม็กซิโกเฉพาะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5b47e-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="5b47e-741">ชนิดการระบุรหัสประจำตัว = "หนังสือเดินทาง"</span><span class="sxs-lookup"><span data-stu-id="5b47e-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="5b47e-742">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="5b47e-742">Issued Date</span></span>
- <span data-ttu-id="5b47e-743">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="5b47e-743">Expiration Date</span></span>

<span data-ttu-id="5b47e-744">พนักงานสามารถประกาศหมายเลขรหัสหลายเลขของชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="5b47e-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="5b47e-745">อย่างไรก็ตาม เฉพาะรายการหนังสือเดินทางที่ใช้งานปัจจุบันจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="5b47e-746">ถ้ารายการหนังสือเดินทางทั้งหมดหมดอายุ หนังสือเดินทางที่ออกครั้งล่าสุดจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="5b47e-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
