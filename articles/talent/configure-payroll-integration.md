---
title: "ตั้งค่าคอนฟิกการรวมค่าจ้างระหว่าง Talent และ Dayforce"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการรวมระหว่าง Microsoft Dynamics 365 for Talent และ Ceridian Dayforce เพื่อให้คุณสามารถประมวลผลการชำระค่าจ้างที่รันได้"
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="32d0b-103">ตั้งค่าคอนฟิกการรวมค่าจ้างระหว่าง Talent และ Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32d0b-104">การรวมระหว่าง Microsoft Dynamics 365 for Talent และ Ceridian Dayforce ต้องอาศัยการตั้งค่าคอนฟิกหลายขั้นตอนที่อธิบายไว้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="32d0b-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="32d0b-105">คุณต้องตั้งค่าคอนฟิกการรวมทั้ง Talent และ Dayforce ก่อนที่คุณจะสามารถประมวลผลการชำระค่าจ้างที่รันได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="32d0b-106">เมื่อคุณใช้บริการเช่น Dayforce เพื่อทำให้การชำระค่าจ้างเสร็จสมบูรณ์ คุณต้องเปิดใช้งานการรวมใน Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="32d0b-107">การรวมจำเป็นต้องมีข้อมูลที่เฉพาะเจาะจงจาก Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="32d0b-108">ดังนั้น คุณต้องตรวจสอบว่า ข้อมูลที่มีการแม็ปกับ Dayforce ถูกตั้งค่าคอนฟิกใน Talent ในลักษณะที่สนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="32d0b-109">การรวมใช้ประเภทที่กว้างของข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="32d0b-110">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="32d0b-110">Human resources data</span></span>
- <span data-ttu-id="32d0b-111">ข้อมูลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-111">Compensation data</span></span>
- <span data-ttu-id="32d0b-112">ข้อมูลค่าจ้าง เช่น รอบการชำระค่าจ้าง รอบระยะเวลาการชำระค่าจ้าง และรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="32d0b-113">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-113">Worker data</span></span>

<span data-ttu-id="32d0b-114">หัวข้อนี้อธิบายขั้นตอนต่างๆ ที่คุณต้องปฏิบัติตามเพื่อเปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="32d0b-115">นอกจากนี้ ยังอธิบายถึงชนิดของข้อมูลและรายละเอียดการตั้งค่าคอนฟิกที่การรวมต้องการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="32d0b-116">เปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-116">Enable the integration</span></span>

<span data-ttu-id="32d0b-117">ใน Talent คุณต้องเปิดใช้งานการรวม และป้อนข้อมูลการตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="32d0b-118">ถ้าคุณต้องการธุรกรรมบัญชีแยกประเภททั่วไปที่จะถูกสร้างให้ถูกนำเข้าไปยัง Microsoft Dynamics 365 for Finance and Operations นอกจากนี้ คุณยังต้องตั้งค่าบัญชีการจัดเก็บ Microsoft Azure และป้อนสตริงการเชื่อมต่อการจัดเก็บ Azure ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="32d0b-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="32d0b-119">เมื่อต้องการเปิดใช้งานการรวมใน Talent ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="32d0b-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="32d0b-120">ในหน้า **การดูแลระบบ** เลือก **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="32d0b-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="32d0b-121">ป้อนปลายทาง File Transfer Protocol (FTP) แบบปลอดภัย และพาธโฟลเดอร์ FTP แบบปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="32d0b-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="32d0b-122">ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่จะเข้าถึงปลายทาง FTP แบบปลอดภัย และโฟลเดอร์พาธ</span><span class="sxs-lookup"><span data-stu-id="32d0b-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="32d0b-123">ทดสอบการเชื่อมต่อ หากจำเป็น และตั้งค่าตัวเลือก **เปิดใช้งานการรวมค่าจ้าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="32d0b-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="32d0b-124">เมื่อเปิดการรวม มีการสร้างแพคเกจการส่งออกข้อมูลและไฟล์ และมีการตั้งค่าความถี่</span><span class="sxs-lookup"><span data-stu-id="32d0b-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="32d0b-125">คุณสามารถเปลี่ยนความถี่นี้ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="32d0b-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบัญชีการจัดเก็บ Azure และสตริงการเชื่อมต่อการจัดเก็บ Azure ดูหัวข้อ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="32d0b-127">เกี่ยวกับบัญชีการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="32d0b-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="32d0b-128">ตั้งค่าคอนฟิกสตริงการเชื่อมต่อการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="32d0b-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="32d0b-129">ตั้งค่าคอนฟิกข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-129">Configure your data</span></span> 

<span data-ttu-id="32d0b-130">ในการประมวลผลค่าจ้าง คุณต้องตั้งค่าคอนฟิกข้อมูลทรัพยากรบุคคลใน Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="32d0b-131">คุณต้องตั้งค่าข้อมูลองค์กร เช่น งาน และตำแหน่ง พร้อมด้วยข้อมูลค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="32d0b-132">ข้อมูลนี้ให้ข้อมูลการจ้างงาน ค่าจ้าง และการหักลด ที่จำเป็นในการสร้างค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="32d0b-133">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="32d0b-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="32d0b-134">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-134">Benefits</span></span> 

<span data-ttu-id="32d0b-135">ทรัพยากรบุคคลให้เครื่องมือสำหรับการตั้งค่าและการบำรุงรักษาของสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงาน ที่หน่วยงานนำเสนอหรือประมวลผลสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="32d0b-136">เมื่อคุณสร้างสวัสดิการ พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="32d0b-137">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-137">Benefit plans</span></span>

- <span data-ttu-id="32d0b-138">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-138">Plan (required)</span></span>
- <span data-ttu-id="32d0b-139">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-139">Type (required)</span></span>
- <span data-ttu-id="32d0b-140">ผลกระทบของค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-140">Payroll impact (required)</span></span>
- <span data-ttu-id="32d0b-141">ขอคืนเงินค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="32d0b-141">Recover arrears</span></span>
- <span data-ttu-id="32d0b-142">วิธีการหักลด</span><span class="sxs-lookup"><span data-stu-id="32d0b-142">Deduction method</span></span>
- <span data-ttu-id="32d0b-143">ระดับความสำคัญการหักลด</span><span class="sxs-lookup"><span data-stu-id="32d0b-143">Deduction priority</span></span>
- <span data-ttu-id="32d0b-144">จำกัดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="32d0b-144">Limit period</span></span>
- <span data-ttu-id="32d0b-145">ยอดวงเงิน</span><span class="sxs-lookup"><span data-stu-id="32d0b-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="32d0b-146">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-146">Benefits</span></span>

- <span data-ttu-id="32d0b-147">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-147">Plan (required)</span></span>
- <span data-ttu-id="32d0b-148">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-148">Type (required)</span></span>
- <span data-ttu-id="32d0b-149">ตัวเลือก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-149">Option (required)</span></span>
- <span data-ttu-id="32d0b-150">รหัสสวัสดิการ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-150">Benefit ID (required)</span></span>
- <span data-ttu-id="32d0b-151">ความถี่</span><span class="sxs-lookup"><span data-stu-id="32d0b-151">Frequency</span></span>
- <span data-ttu-id="32d0b-152">ข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-152">Basis</span></span>
- <span data-ttu-id="32d0b-153">ยอดเงินหรืออัตรา</span><span class="sxs-lookup"><span data-stu-id="32d0b-153">Amount or rate</span></span>
- <span data-ttu-id="32d0b-154">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="32d0b-155">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="32d0b-155">Supported frequencies</span></span> 

- <span data-ttu-id="32d0b-156">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="32d0b-156">Weekly</span></span>
- <span data-ttu-id="32d0b-157">ทุกสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="32d0b-157">Bi-weekly</span></span>
- <span data-ttu-id="32d0b-158">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-158">Semi-monthly</span></span>
- <span data-ttu-id="32d0b-159">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="32d0b-160">ฐานที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="32d0b-160">Supported bases</span></span> 

- <span data-ttu-id="32d0b-161">ยอดเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-161">Fixed amount</span></span>
- <span data-ttu-id="32d0b-162">เปอร์เซ็นต์ของรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-162">Percent of earnings</span></span>
- <span data-ttu-id="32d0b-163">ชั่วโมงที่มีประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-163">Productive hours</span></span>

<span data-ttu-id="32d0b-164">Dayforce สร้างการหักลดต่อไปนี้ โดยขึ้นอยู่กับผลกระทบของค่าจ้างที่กำหนดในแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="32d0b-165">การเลือกใน Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-165">Selection in Talent</span></span>        | <span data-ttu-id="32d0b-166">ผลลัพธ์ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="32d0b-167">None</span><span class="sxs-lookup"><span data-stu-id="32d0b-167">None</span></span>                       | <span data-ttu-id="32d0b-168">ไม่มีการสร้างการหักลด</span><span class="sxs-lookup"><span data-stu-id="32d0b-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="32d0b-169">การหักลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-169">Deduction only</span></span>             | <span data-ttu-id="32d0b-170">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="32d0b-171">การจ่ายเงินสมทบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-171">Contribution only</span></span>          | <span data-ttu-id="32d0b-172">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="32d0b-173">การหักลดและการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="32d0b-173">Deduction and contribution</span></span> | <span data-ttu-id="32d0b-174">การหักลดพนักงานและนายจ้างจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="32d0b-175">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนด และจัดการโปรแกรมสวัสดิการ ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="32d0b-176">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="32d0b-177">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="32d0b-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="32d0b-178">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="32d0b-179">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="32d0b-180">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-180">Compensation</span></span> 

<span data-ttu-id="32d0b-181">การจัดการค่าตอบแทนจะใช้ควบคุมการจัดส่งของค่าจ้างพื้นฐานและเงินรางวัล</span><span class="sxs-lookup"><span data-stu-id="32d0b-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="32d0b-182">ค่าจ้างพื้นฐานคงที่ของพนักงานและการขึ้นค่าตอบแทนตามผลงานจะถูกควบคุมโดยใช้แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="32d0b-183">ค่าจ้างจูงใจเช่นการชำระเงินโบนัส รางวัลตามผลการปฏิบัติงาน สิทธิในการซื้อหุ้น การให้หุ้น รางวัลที่จ่ายครั้งเดียว โดยใช้แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="32d0b-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="32d0b-184">Dayforce ใช้ข้อมูลค่าตอบแทนที่คำนวณอัตรารายชั่วโมงหรือรายปีของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="32d0b-185">จำเป็นต้องมีแผนค่าตอบแทนคงที่และการแปลงอัตราค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="32d0b-186">พนักงานต้องเชื่อมโยงกับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="32d0b-187">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแผนค่าตอบแทน โปรดดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="32d0b-188">สร้างแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="32d0b-189">สร้างแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="32d0b-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="32d0b-190">พัฒนาโครงสร้างและแผนเงินเดือน/ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="32d0b-191">ประมวลผลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="32d0b-192">กำหนดกระบวนการของค่าตอบแทนและคำนวณผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="32d0b-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="32d0b-193">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="32d0b-194">การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="32d0b-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="32d0b-195">งาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-195">Jobs</span></span> 

<span data-ttu-id="32d0b-196">งานเป็นชุดของงานและความรับผิดชอบที่ถูกระบุของบุคคลที่ดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="32d0b-197">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="32d0b-198">การตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="32d0b-199">กำหนดงานใหม่</span><span class="sxs-lookup"><span data-stu-id="32d0b-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="32d0b-200">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="32d0b-200">Positions</span></span>

<span data-ttu-id="32d0b-201">ตำแหน่งคือแต่ละอินสแตนซ์ของงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="32d0b-202">ตัวอย่างเช่น ตำแหน่ง "ผู้จัดการฝ่ายขาย (ตะวันออก)" เป็นหนึ่งในตำแหน่งที่เชื่อมโยงกับงาน "ผู้จัดการฝ่ายขาย"</span><span class="sxs-lookup"><span data-stu-id="32d0b-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="32d0b-203">ตำแหน่งมีอยู่ในแผนก</span><span class="sxs-lookup"><span data-stu-id="32d0b-203">A position exists in a department.</span></span> <span data-ttu-id="32d0b-204">สามารถเชื่อมโยงผู้ปฏิบัติงานหนึ่งรายกับแต่ละตำแหน่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="32d0b-205">เก็บข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ไว้ เมื่อคุณตั้งค่าตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="32d0b-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="32d0b-206">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-206">Position (required)</span></span>
- <span data-ttu-id="32d0b-207">คำอธิบาย (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-207">Description (required)</span></span>
- <span data-ttu-id="32d0b-208">งาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-208">Job (required)</span></span>
- <span data-ttu-id="32d0b-209">แผนก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-209">Department (required)</span></span>
- <span data-ttu-id="32d0b-210">ชนิดตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-210">Position type (required)</span></span>
- <span data-ttu-id="32d0b-211">จำนวนบุคลากรเทียบเท่าเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="32d0b-211">Full-time equivalent</span></span>
- <span data-ttu-id="32d0b-212">ชั่วโมงปกติรายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="32d0b-213">ชำระโดยนิติบุคคล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="32d0b-214">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-214">Pay cycle (required)</span></span>
- <span data-ttu-id="32d0b-215">มิติทางการเงินเริ่มต้น – ศูนย์ต้นทุน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="32d0b-216">การมอบหมายผู้ปฏิบัติงาน – ผู้ปฏิบัติงาน การเริ่มต้นการกำหนด การสิ้นสุดการกำหนด รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="32d0b-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="32d0b-217">ถ้าตำแหน่งหลายตำแหน่งในแผนกเดียวกันเกี่ยวข้องกับงานเดียวกัน จะมีการรวมลงในตำแหน่งหนึ่งๆ ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="32d0b-218">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="32d0b-219">จัดระเบียบบุคลากรของคุณโดยใช้แผนก งาน และตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="32d0b-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="32d0b-220">ตั้งค่าตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="32d0b-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="32d0b-221">แผนก</span><span class="sxs-lookup"><span data-stu-id="32d0b-221">Departments</span></span>

<span data-ttu-id="32d0b-222">แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="32d0b-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="32d0b-223">แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="32d0b-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="32d0b-224">คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="32d0b-225">แผนกอาจมีความรับผิดชอบกำไรและขาดทุน</span><span class="sxs-lookup"><span data-stu-id="32d0b-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="32d0b-226">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="32d0b-227">สร้างแผนกและการเชื่อมโยงกับลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="32d0b-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="32d0b-228">กำหนดฝ่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="32d0b-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="32d0b-229">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="32d0b-230">รอบการชำระค่าจ้างกำหนดความถี่ในการรันค่าจ้าง และจำนวนวันที่เจาะจงเมื่อผู้ปฏิบัติงานได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="32d0b-231">ตัวอย่างเช่น รอบการชำระค่าจ้างอาจเป็นรายเดือน และพนักงานอาจได้รับค่าจ้างในวันสุดท้ายของเดือนนั้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="32d0b-232">อีกทางหนึ่งคือ รอบการชำระค่าจ้างอาจเป็นรายสัปดาห์ และพนักงานอาจได้รับค่าจ้างในวันอังคารหลังจากจุดสิ้นสุดของรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="32d0b-233">รอบการชำระค่าจ้างถูกกำหนดให้กับตำแหน่ง เพื่อควบคุมเวลาที่ผู้ปฏิบัติงานในตำแหน่งเหล่านั้นได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="32d0b-234">หลังจากที่คุณสร้างรอบการชำระค่าจ้าง คุณสามารถสร้างรอบระยะเวลาการชำระค่าจ้างสำหรับแต่ละรอบได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="32d0b-235">รอบการชำระค่าจ้างแต่ละรอบรวมถึงวันที่ของการชำระเงินเริ่มต้นที่ยึดตามข้อมูลที่คุณให้</span><span class="sxs-lookup"><span data-stu-id="32d0b-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="32d0b-236">อย่างไรก็ตาม คุณสามารถแก้ไขวันที่การชำระเงินเริ่มต้นได้ในรอบการชำระค่าจ้างเพื่อให้อนุญาตการยกเว้น เช่น เมื่อวันที่ชำระเงินตรงกับวันหยุด</span><span class="sxs-lookup"><span data-stu-id="32d0b-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="32d0b-237">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="32d0b-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="32d0b-238">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-238">Pay cycle (required)</span></span>
- <span data-ttu-id="32d0b-239">ความถี่ของรอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="32d0b-240">วันที่เริ่มรอบระยะเวลา (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="32d0b-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="32d0b-241">วันที่การชำระเงินเริ่มต้น (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="32d0b-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="32d0b-242">ข้อมูลนี้ถูกรวมเข้ากับ Dayforce เป็นกลุ่มค่าจ้าง และจะถูกแยกตามประเทศหรือภูมิภาคสำหรับรอบการชำระค่าจ้างแต่ละรอบ</span><span class="sxs-lookup"><span data-stu-id="32d0b-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="32d0b-243">ต้องมีการสร้างรอบระยะเวลาการชำระค่าจ้างอย่างน้อยหนึ่งรายการ ก่อนที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="32d0b-244">Dayforce สร้างปฏิทินกลุ่มค่าจ้างและวันที่ในการชำระเงิน โดยยึดตามวันที่เริ่มต้นของรอบระยะเวลาการชำระค่าจ้างแรก และวันที่ชำระเงินเริ่มต้นที่ตั้งค่าใน Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="32d0b-245">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-245">Earning codes</span></span>

<span data-ttu-id="32d0b-246">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="32d0b-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="32d0b-247">รหัสมีพารามิเตอร์ต่าง ๆ ที่เกี่ยวข้องกับรายได้ เช่น แต่ละ กฎทางบัญชี กฎภาษี และรายงานความต้องการและความสามารถในการรวมได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="32d0b-248">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="32d0b-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="32d0b-249">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-249">Earning Code (required)</span></span>
- <span data-ttu-id="32d0b-250">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-250">Description</span></span>
- <span data-ttu-id="32d0b-251">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="32d0b-251">Unit of measure</span></span>
- <span data-ttu-id="32d0b-252">ประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="32d0b-253">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-253">Worker data</span></span>

<span data-ttu-id="32d0b-254">เรกคอร์ดสำหรับชนิดต่างๆ ของผู้ปฏิบัติงานที่คุณมี มีความสำคัญสำหรับระบบค่าจ้างและทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="32d0b-255">ข้อมูลที่คุณป้อนสามารถใช้ติดตามผู้ปฏิบัติงานและข้อมูลส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="32d0b-256">คุณสามารถรักษาข้อมูลต่อไปนี้สำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="32d0b-257">**พื้นฐาน** – รักษาข้อมูลพื้นฐานเกี่ยวกับผู้ปฏิบัติงาน เช่น ข้อมูลการติดต่อ ข้อมูลทางประชากรศาสตร์ ข้อมูลการระบุรหัสประจำตัว ข้อมูลครอบครัว สถานะการรับราชการทหาร ข้อมูลคนต่างด้าว และผู้ติดต่อได้ในกรณีฉุกเฉินและส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="32d0b-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="32d0b-258">**การจ้างงาน** – รักษาข้อมูลเกี่ยวกับการจ้างงานของผู้ปฏิบัติงาน เช่น บริษัท หรือสังกัดองค์กร การมอบหมายตำแหน่งงาน วันที่เริ่มต้นและสิ้นสุด สิทธิการทำงาน เงื่อนไขในการจ้างงาน เงินบำนาญ วันหยุดพักผ่อน และข้อมูลการย้ายสถานที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="32d0b-259">**การลางานและการขาดงาน** – รักษาข้อมูลเกี่ยวกับการขาดงานของผู้ปฏิบัติงาน เช่น ปฏิทินการทำงาน ธุรกรรมการขาดงาน และการตั้งค่าการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="32d0b-260">**ค่าตอบแทนและค่าจ้าง** – รักษาข้อมูลเกี่ยวกับแผนค่าตอบแทนของผู้ปฏิบัติงานและข้อมูลค่าจ้าง เช่น การลงทะเบียนสำหรับแผน รางวัล ประสิทธิภาพ ค่าคอมมิชชัน ข้อมูลภาษี การเกษียณอายุ และการหักเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="32d0b-261">เมื่อคุณป้อนข้อมูลผู้ปฏิบัติงาน พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="32d0b-262">ข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="32d0b-262">General information</span></span>

- <span data-ttu-id="32d0b-263">หมายเลขบุคลากร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-263">Personnel number (required)</span></span>
- <span data-ttu-id="32d0b-264">ชื่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-264">First name (required)</span></span>
- <span data-ttu-id="32d0b-265">นามสกุล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-265">Last name (required)</span></span>
- <span data-ttu-id="32d0b-266">ชื่อกลาง</span><span class="sxs-lookup"><span data-stu-id="32d0b-266">Middle name</span></span>
- <span data-ttu-id="32d0b-267">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-267">Seniority date</span></span>
- <span data-ttu-id="32d0b-268">เรียกว่า</span><span class="sxs-lookup"><span data-stu-id="32d0b-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="32d0b-269">ข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="32d0b-269">Personal information</span></span>

- <span data-ttu-id="32d0b-270">สถานภาพการสมรส (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-270">Marital status (required)</span></span>
- <span data-ttu-id="32d0b-271">วันที่เกิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-271">Birth date (required)</span></span>
- <span data-ttu-id="32d0b-272">เพศ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-272">Gender (required)</span></span>
- <span data-ttu-id="32d0b-273">บุคคลทุพพลภาพ</span><span class="sxs-lookup"><span data-stu-id="32d0b-273">Person with disabilities</span></span>
- <span data-ttu-id="32d0b-274">สัญชาติประเทศภูมิภาค (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="32d0b-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="32d0b-275">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="32d0b-275">Address information</span></span>

- <span data-ttu-id="32d0b-276">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-276">Primary (required)</span></span>
- <span data-ttu-id="32d0b-277">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-277">Country/region (required)</span></span>
- <span data-ttu-id="32d0b-278">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-278">Postal code (required)</span></span>
- <span data-ttu-id="32d0b-279">หมายเลขถนน (จำเป็น) (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="32d0b-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="32d0b-280">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="32d0b-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="32d0b-281">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-281">City (required)</span></span>
- <span data-ttu-id="32d0b-282">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-282">State (required)</span></span>
- <span data-ttu-id="32d0b-283">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="32d0b-284">ข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="32d0b-284">Contact information</span></span> 

- <span data-ttu-id="32d0b-285">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-285">Primary (required)</span></span>
- <span data-ttu-id="32d0b-286">หมายเลขผู้ติดต่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-286">Contact number (required)</span></span>
- <span data-ttu-id="32d0b-287">การขยาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="32d0b-288">ข้อมูลค่าจ้างและรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-288">Payroll information and earning codes</span></span>

<span data-ttu-id="32d0b-289">พนักงานอาจถูกกำหนดรายได้เฉพาะที่ความถี่ที่กำหนดของการชำระเงิน และมีวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="32d0b-290">ฟิลด์ต่อไปนี้จะใช้ใน Dayforce เพื่อช่วยในการรับประกันว่า การกำหนดลักษณะและการตั้งค่าเหล่านั้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="32d0b-291">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-291">Earning codes</span></span>

- <span data-ttu-id="32d0b-292">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-292">Position (required)</span></span>
- <span data-ttu-id="32d0b-293">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-293">Earning Code (required)</span></span>
- <span data-ttu-id="32d0b-294">ความถี่ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-294">Frequency (required)</span></span>
- <span data-ttu-id="32d0b-295">จำนวน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="32d0b-296">ข้อมูลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-296">Payroll information</span></span>

- <span data-ttu-id="32d0b-297">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="32d0b-297">Payment Method</span></span>
- <span data-ttu-id="32d0b-298">ภูมิภาคเศรษฐกิจ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-298">Economic Region (required)</span></span>
- <span data-ttu-id="32d0b-299">รหัสสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-299">Employee Benefits ID</span></span>
- <span data-ttu-id="32d0b-300">หมายเลขรหัสประจำชาติ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-300">National ID Number (required)</span></span>
- <span data-ttu-id="32d0b-301">หมายเลขการรับราชการทหาร</span><span class="sxs-lookup"><span data-stu-id="32d0b-301">Military Service Number</span></span>
- <span data-ttu-id="32d0b-302">รหัสกะ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-302">Shift ID (required)</span></span>
- <span data-ttu-id="32d0b-303">หมายเลขภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-303">Tax Number (required)</span></span>
- <span data-ttu-id="32d0b-304">รหัสสหภาพ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-304">Union ID (required)</span></span>
- <span data-ttu-id="32d0b-305">รหัสวันทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-305">Work Day ID (required)</span></span>
- <span data-ttu-id="32d0b-306">หมายเลขใบอนุญาตทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="32d0b-307">สำหรับวิธีการชำระเงิน เม็กซิโกสนับสนุน **เงินสด** **เช็ค** (เช็คจริงของบริษัท) และ **การชำระเงินทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="32d0b-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="32d0b-308">ถ้าไม่มีการระบุวิธีการชำระเงิน **เช็ค** จะถูกใช้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="32d0b-309">รายละเอียดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-309">Employment details</span></span>

<span data-ttu-id="32d0b-310">ประวัติรายละเอียดตการจ้างงานถูกใช้เป็นข้อมูลสำคัญในการสืบทอดการพนักงานจ้างงานของพนักงาน การหยุดชะงัก และสถานะการจ้างงานใหม่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="32d0b-311">Dayforce สนับสนุนเรกคอร์ดการจ้างงานที่ใช้งานอยู่เพียงรายการเดียวในแต่ละครั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="32d0b-312">วันที่เริ่มต้นการจ้างงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-312">Employment start date (required)</span></span>
- <span data-ttu-id="32d0b-313">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-313">Employment end date</span></span>
- <span data-ttu-id="32d0b-314">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-314">Start date</span></span>
- <span data-ttu-id="32d0b-315">วันที่เริ่มต้นที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="32d0b-315">Adjusted start date</span></span>
- <span data-ttu-id="32d0b-316">วันที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="32d0b-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="32d0b-317">เหตุผลที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="32d0b-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="32d0b-318">วันสำคัญของพนักงานได้รับมาโดยใช้ข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="32d0b-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="32d0b-319">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-319">Talent</span></span>                | <span data-ttu-id="32d0b-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d0b-321">วันที่จ้างงานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="32d0b-321">Most recent hire date</span></span> | <span data-ttu-id="32d0b-322">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="32d0b-323">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-323">Termination date</span></span>      | <span data-ttu-id="32d0b-324">วันที่สิ้นสุดการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="32d0b-325">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-325">Start date</span></span>            | <span data-ttu-id="32d0b-326">วันที่เริ่มต้นที่ปรับปรุงแล้ว วันที่เริ่มต้น หรือการเริ่มต้นการจ้างงานของเรกคอร์ประวัติการจ้างงานที่ไม่ได้ใช้งานอยู่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="32d0b-327">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="32d0b-327">Original hire date</span></span>    | <span data-ttu-id="32d0b-328">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานแรกสุด</span><span class="sxs-lookup"><span data-stu-id="32d0b-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="32d0b-329">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-329">Compensation</span></span>

<span data-ttu-id="32d0b-330">แผนค่าตอบแทนคงต้องเชื่อมโยงกับตำแหน่งหลักของพนักงานทุกตำแหน่ง ตลอดรอบระยะเวลาการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="32d0b-331">รอบระยะเวลานี้เริ่มต้นในวันที่ที่พนักงานถูกจ้างงาน (หรือวันที่เริ่มต้นการจ้างงาน) และดำเนินต่อไปจนกว่าจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="32d0b-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="32d0b-332">วันที่มีผลบังคับใช้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-332">Effective Date (required)</span></span>
- <span data-ttu-id="32d0b-333">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="32d0b-333">Expiration date</span></span>
- <span data-ttu-id="32d0b-334">อัตราการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-334">Pay Rate (required)</span></span>
- <span data-ttu-id="32d0b-335">การแปลงอัตราค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="32d0b-336">จำนวนเทียบเท่ารายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="32d0b-337">จำนวนเทียบเท่ารายชั่วโมง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="32d0b-338">ถ้าพนักงานรายชั่วโมงมีตำแหน่งหลายตำแหน่ง ค่าตอบแทนคงที่ของตำแหน่งหลักจะถูกนำเข้าใน Dayforce เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="32d0b-339">สำหรับตำแหน่งที่ไม่ใช่ตำแหน่งหลัก อัตรารายชั่วโมงถูกบันทึกลงในตำแหน่งที่สอดคล้องกันใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="32d0b-340">ถ้าพนักงานประจำมีตำแหน่งหลายตำแหน่ง จะได้รับอัตราชั่วโมงสะสมและเงินเดือนต่อปีระหว่างตำแหน่งที่ใช้งานอยู่ทั้งหมด และถูกใช้เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="32d0b-341">หมายเลขรหัส</span><span class="sxs-lookup"><span data-stu-id="32d0b-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="32d0b-342">ตัวระบุประกันสังคม</span><span class="sxs-lookup"><span data-stu-id="32d0b-342">Social Security identifier</span></span> 

<span data-ttu-id="32d0b-343">พนักงานทุกคนต้องมีตัวระบุหลักหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="32d0b-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="32d0b-344">ตัวระบุนี้ต้องเป็นชนิดรหัส **SSN**</span><span class="sxs-lookup"><span data-stu-id="32d0b-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="32d0b-345">ใน Dayforce จะได้รับมาโดยอัตโนมัติเป็นตัวระบุประกันสังคมของพนักงานที่จำเป็นสำหรับการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="32d0b-346">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-346">Primary (required)</span></span>
- <span data-ttu-id="32d0b-347">ชนิดข้อมูลประจำตัว = "SSN"</span><span class="sxs-lookup"><span data-stu-id="32d0b-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="32d0b-348">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="32d0b-348">Issued Date</span></span>
- <span data-ttu-id="32d0b-349">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="32d0b-349">Expiration Date</span></span>

<span data-ttu-id="32d0b-350">พนักงานสามารถประกาศหมายเลขการระบุรหัสประจำตัวหลายเลขของชนิดการระบุรหัสประจำตัว **SSN**</span><span class="sxs-lookup"><span data-stu-id="32d0b-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="32d0b-351">อย่างไรก็ตาม เฉพาะเรกคอร์ดที่ถูกทำเครื่องหมายเป็น **หลัก** ถูกรวมเข้ากับ Dayforce ไม่ว่าหมายเลขจะใช้งานอยู่ หรือหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="32d0b-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="32d0b-352">บัญชีธนาคารและการเบิกจ่าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="32d0b-353">ต้องป้อนข้อมูลบัญชีธนาคารที่ถูกต้องสำหรับพนักงานใดๆ ที่เลือกที่จะรับการชำระเงินผ่านการโอนย้ายของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="32d0b-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="32d0b-354">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-354">Talent</span></span>                         | <span data-ttu-id="32d0b-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d0b-356">หมายเลขบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="32d0b-357">รหัส SWIFT (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-357">SWIFT code (required)</span></span>          | <span data-ttu-id="32d0b-358">ฟิลด์ **รหัสธนาคาร** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="32d0b-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="32d0b-359">หมายเลขสาขา (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="32d0b-360">ชนิดของบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-360">Bank account type (required)</span></span>   | <span data-ttu-id="32d0b-361">ฟิลด์ **ชนิดของบัญชี** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="32d0b-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="32d0b-362">ค่าที่ได้รับการสนับสนุนได้แก่ **การตรวจสอบ** และ **ค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="32d0b-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="32d0b-363">พนักงานที่เลือกจะรับการชำระผ่านการโอนผ่านบัญชีธนาคาร ต้องมีลิงก์ไปยังบัญชีเงินส่วนที่เหลือที่อยู่ภายใต้นิติบุคคลที่มีที่อยู่หลักในเม็กซิโก และเชื่อมโยงกับบัญชีธนาคารที่ถูกต้องจากธนาคารเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="32d0b-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="32d0b-364">บัญชีที่ไม่ใช่เงินส่วนที่เหลืออื่นๆ ทั้งหมดจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="32d0b-365">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="32d0b-365">Address information</span></span>

<span data-ttu-id="32d0b-366">พนักงานทุกคนต้องมีสถานที่หลักหนึ่งแห่ง</span><span class="sxs-lookup"><span data-stu-id="32d0b-366">Every employee must have one primary location.</span></span> <span data-ttu-id="32d0b-367">ใน Dayforce สถานที่นี้จะใช้เพื่อกำหนดที่พักอาศัยหลักของพนักงานสำหรับวัตถุประสงค์ด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="32d0b-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="32d0b-368">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-368">Primary (required)</span></span>
- <span data-ttu-id="32d0b-369">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-369">Country/region (required)</span></span>
- <span data-ttu-id="32d0b-370">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="32d0b-371">ถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-371">Street (required)</span></span>
- <span data-ttu-id="32d0b-372">หมายเลขถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-372">Street Number (required)</span></span>
- <span data-ttu-id="32d0b-373">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="32d0b-373">Building Complement</span></span>
- <span data-ttu-id="32d0b-374">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-374">City (required)</span></span>
- <span data-ttu-id="32d0b-375">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-375">State (required)</span></span>
- <span data-ttu-id="32d0b-376">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="32d0b-377">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="32d0b-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="32d0b-378">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในสหรัฐอเมริกาและแคนาดา ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="32d0b-379">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-379">Departments are required on positions.</span></span>
- <span data-ttu-id="32d0b-380">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="32d0b-381">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-381">Job types</span></span>

<span data-ttu-id="32d0b-382">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="32d0b-383">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="32d0b-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="32d0b-384">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="32d0b-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="32d0b-385">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="32d0b-386">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-387">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-387">Job type</span></span>   | <span data-ttu-id="32d0b-388">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="32d0b-389">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="32d0b-389">Hourly</span></span>     | <span data-ttu-id="32d0b-390">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="32d0b-390">Hourly</span></span>      |
| <span data-ttu-id="32d0b-391">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-391">Salaried</span></span>   | <span data-ttu-id="32d0b-392">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="32d0b-393">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-393">Position types</span></span> 

<span data-ttu-id="32d0b-394">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="32d0b-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="32d0b-395">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="32d0b-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="32d0b-396">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-397">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="32d0b-397">Position type</span></span>   | <span data-ttu-id="32d0b-398">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="32d0b-399">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="32d0b-399">Full-time</span></span>       | <span data-ttu-id="32d0b-400">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="32d0b-400">Full time employee</span></span> |
| <span data-ttu-id="32d0b-401">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="32d0b-401">Part-time</span></span>       | <span data-ttu-id="32d0b-402">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="32d0b-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="32d0b-403">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="32d0b-403">Reason codes</span></span>

<span data-ttu-id="32d0b-404">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="32d0b-405">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="32d0b-406">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-407">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="32d0b-407">Reason code</span></span>    | <span data-ttu-id="32d0b-408">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-408">Description</span></span>      | <span data-ttu-id="32d0b-409">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="32d0b-410">การลาออก</span><span class="sxs-lookup"><span data-stu-id="32d0b-410">RESIGNATION</span></span>    | <span data-ttu-id="32d0b-411">การลาออก</span><span class="sxs-lookup"><span data-stu-id="32d0b-411">Resignation</span></span>      | <span data-ttu-id="32d0b-412">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-412">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-413">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-413">TERMINATION</span></span>    | <span data-ttu-id="32d0b-414">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-414">Termination</span></span>      | <span data-ttu-id="32d0b-415">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-415">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-416">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-416">RETIREMENT</span></span>     | <span data-ttu-id="32d0b-417">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-417">Retirement</span></span>       | <span data-ttu-id="32d0b-418">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-418">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-419">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-419">OTHER</span></span>          | <span data-ttu-id="32d0b-420">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-420">Other Reasons</span></span>    | <span data-ttu-id="32d0b-421">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-421">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-422">ความตาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-422">DEATH</span></span>          | <span data-ttu-id="32d0b-423">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="32d0b-423">Death</span></span>            | <span data-ttu-id="32d0b-424">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-424">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="32d0b-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="32d0b-426">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="32d0b-426">Leave of Absence</span></span> | <span data-ttu-id="32d0b-427">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-427">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="32d0b-428">CONTRACTEND</span></span>    | <span data-ttu-id="32d0b-429">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="32d0b-429">End of Contract</span></span>  | <span data-ttu-id="32d0b-430">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-430">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="32d0b-431">SALARYCHANGE</span></span>   | <span data-ttu-id="32d0b-432">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-432">Change of Salary</span></span> | <span data-ttu-id="32d0b-433">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="32d0b-434">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="32d0b-434">Marital status</span></span>

<span data-ttu-id="32d0b-435">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="32d0b-436">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="32d0b-437">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-437">Talent</span></span>                 | <span data-ttu-id="32d0b-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="32d0b-439">สมรส</span><span class="sxs-lookup"><span data-stu-id="32d0b-439">Married</span></span>                | <span data-ttu-id="32d0b-440">สมรส</span><span class="sxs-lookup"><span data-stu-id="32d0b-440">Married</span></span>              |
| <span data-ttu-id="32d0b-441">โสด</span><span class="sxs-lookup"><span data-stu-id="32d0b-441">Single</span></span>                 | <span data-ttu-id="32d0b-442">โสด</span><span class="sxs-lookup"><span data-stu-id="32d0b-442">Single</span></span>               |
| <span data-ttu-id="32d0b-443">หม้าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-443">Widowed</span></span>                | <span data-ttu-id="32d0b-444">หม้าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-444">Widowed</span></span>              |
| <span data-ttu-id="32d0b-445">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-445">Divorced</span></span>               | <span data-ttu-id="32d0b-446">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-446">Divorced</span></span>             |
| <span data-ttu-id="32d0b-447">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="32d0b-447">Registered Partnership</span></span> | <span data-ttu-id="32d0b-448">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="32d0b-448">Domestic Partnership</span></span> |
| <span data-ttu-id="32d0b-449">None</span><span class="sxs-lookup"><span data-stu-id="32d0b-449">None</span></span>                   | <span data-ttu-id="32d0b-450">None</span><span class="sxs-lookup"><span data-stu-id="32d0b-450">None</span></span>                 |
| <span data-ttu-id="32d0b-451">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-451">Cohabiting</span></span>             | <span data-ttu-id="32d0b-452">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="32d0b-453">เพศ</span><span class="sxs-lookup"><span data-stu-id="32d0b-453">Gender</span></span>

<span data-ttu-id="32d0b-454">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="32d0b-455">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="32d0b-456">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-456">Talent</span></span>       | <span data-ttu-id="32d0b-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="32d0b-458">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-458">Male</span></span>         | <span data-ttu-id="32d0b-459">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-459">Male</span></span>            |
| <span data-ttu-id="32d0b-460">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="32d0b-460">Female</span></span>       | <span data-ttu-id="32d0b-461">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="32d0b-461">Female</span></span>          |
| <span data-ttu-id="32d0b-462">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="32d0b-462">Non-specific</span></span> | <span data-ttu-id="32d0b-463">*ไม่สนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="32d0b-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="32d0b-464">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-464">Earning codes</span></span>

<span data-ttu-id="32d0b-465">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="32d0b-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="32d0b-466">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="32d0b-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="32d0b-467">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="32d0b-468">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="32d0b-468">Supported frequencies</span></span>

- <span data-ttu-id="32d0b-469">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="32d0b-469">All</span></span>
- <span data-ttu-id="32d0b-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="32d0b-470">EVERYPAY</span></span>
- <span data-ttu-id="32d0b-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="32d0b-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="32d0b-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="32d0b-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="32d0b-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="32d0b-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="32d0b-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-474">1OFMTH</span></span>
- <span data-ttu-id="32d0b-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-475">LASTOFMTH</span></span>
- <span data-ttu-id="32d0b-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-476">2OFMTH</span></span>
- <span data-ttu-id="32d0b-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-477">3OFMTH</span></span>
- <span data-ttu-id="32d0b-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-478">4OFMTH</span></span>
- <span data-ttu-id="32d0b-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-479">5OFMTH</span></span>
- <span data-ttu-id="32d0b-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-480">1N2OFMTH</span></span>
- <span data-ttu-id="32d0b-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-481">3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-482">1N3OFMTH</span></span>
- <span data-ttu-id="32d0b-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-483">1N4OFMTH</span></span>
- <span data-ttu-id="32d0b-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-484">2N3OFMTH</span></span>
- <span data-ttu-id="32d0b-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-485">2N4OFMTH</span></span>
- <span data-ttu-id="32d0b-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="32d0b-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="32d0b-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="32d0b-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="32d0b-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="32d0b-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="32d0b-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="32d0b-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="32d0b-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="32d0b-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="32d0b-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="32d0b-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="32d0b-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="32d0b-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="32d0b-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="32d0b-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="32d0b-498">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="32d0b-498">Addresses</span></span>

<span data-ttu-id="32d0b-499">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="32d0b-500">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="32d0b-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="32d0b-501">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-501">Talent</span></span>          | <span data-ttu-id="32d0b-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="32d0b-503">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="32d0b-503">Country/Region</span></span>  | <span data-ttu-id="32d0b-504">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="32d0b-504">Country Code</span></span>          |
| <span data-ttu-id="32d0b-505">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="32d0b-505">Zip/Postal Code</span></span> | <span data-ttu-id="32d0b-506">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="32d0b-506">Postal Code</span></span>           |
| <span data-ttu-id="32d0b-507">สถานะ</span><span class="sxs-lookup"><span data-stu-id="32d0b-507">State</span></span>           | <span data-ttu-id="32d0b-508">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="32d0b-508">State Code</span></span>            |
| <span data-ttu-id="32d0b-509">เมือง</span><span class="sxs-lookup"><span data-stu-id="32d0b-509">City</span></span>            | <span data-ttu-id="32d0b-510">เมือง</span><span class="sxs-lookup"><span data-stu-id="32d0b-510">City</span></span>                  |
| <span data-ttu-id="32d0b-511">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="32d0b-511">County</span></span>          | <span data-ttu-id="32d0b-512">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="32d0b-512">County (Municipality)</span></span> |
| <span data-ttu-id="32d0b-513">ถนน</span><span class="sxs-lookup"><span data-stu-id="32d0b-513">Street</span></span>          | <span data-ttu-id="32d0b-514">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="32d0b-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="32d0b-515">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="32d0b-515">Tax regions</span></span>

<span data-ttu-id="32d0b-516">ภูมิภาคการเก็บภาษีถูกใช้เพื่อกำหนดภาษีที่เหมาะสมที่ควรนำมาใช้ในระหว่างการสร้างระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="32d0b-517">ภูมิภาคการเก็บภาษีถูกแม็ปไปยัง Dayforce เป็นที่อยู่ของสถานที่</span><span class="sxs-lookup"><span data-stu-id="32d0b-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="32d0b-518">ภูมิภาคการเก็บภาษีเริ่มต้นต้องเชื่อมโยงกับตำแหน่งงานที่ใช้งานอยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="32d0b-519">ภูมิภาคการเก็บภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-519">Tax region (required)</span></span>
- <span data-ttu-id="32d0b-520">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-520">Country/Region (required)</span></span>
- <span data-ttu-id="32d0b-521">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-521">State (required)</span></span>
- <span data-ttu-id="32d0b-522">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="32d0b-522">County</span></span> 
- <span data-ttu-id="32d0b-523">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="32d0b-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="32d0b-524">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="32d0b-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="32d0b-525">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในเม็กซิโก ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32d0b-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="32d0b-526">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-526">Departments are required on positions.</span></span>
- <span data-ttu-id="32d0b-527">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="32d0b-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="32d0b-528">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-528">Job types</span></span>

<span data-ttu-id="32d0b-529">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="32d0b-530">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="32d0b-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="32d0b-531">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="32d0b-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="32d0b-532">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="32d0b-533">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-534">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-534">Job type</span></span>   | <span data-ttu-id="32d0b-535">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="32d0b-536">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="32d0b-536">Hourly</span></span>     | <span data-ttu-id="32d0b-537">MX รายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="32d0b-537">MX Hourly</span></span>   |
| <span data-ttu-id="32d0b-538">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-538">Salaried</span></span>   | <span data-ttu-id="32d0b-539">MX รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="32d0b-540">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-540">Position types</span></span> 

<span data-ttu-id="32d0b-541">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="32d0b-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="32d0b-542">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="32d0b-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="32d0b-543">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-544">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="32d0b-544">Position type</span></span>   | <span data-ttu-id="32d0b-545">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="32d0b-546">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="32d0b-546">Full-time</span></span>       | <span data-ttu-id="32d0b-547">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="32d0b-547">Full time employee</span></span> |
| <span data-ttu-id="32d0b-548">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="32d0b-548">Part-time</span></span>       | <span data-ttu-id="32d0b-549">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="32d0b-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="32d0b-550">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="32d0b-550">Reason codes</span></span>

<span data-ttu-id="32d0b-551">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="32d0b-552">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="32d0b-553">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-554">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="32d0b-554">Reason code</span></span>            | <span data-ttu-id="32d0b-555">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-555">Description</span></span>                    | <span data-ttu-id="32d0b-556">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="32d0b-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="32d0b-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="32d0b-558">การออกก่อนค่าจ้างแรก</span><span class="sxs-lookup"><span data-stu-id="32d0b-558">Departure before first payroll</span></span> | <span data-ttu-id="32d0b-559">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-559">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-560">การลาออก</span><span class="sxs-lookup"><span data-stu-id="32d0b-560">RESIGNATION</span></span>            | <span data-ttu-id="32d0b-561">การลาออก</span><span class="sxs-lookup"><span data-stu-id="32d0b-561">Resignation</span></span>                    | <span data-ttu-id="32d0b-562">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-562">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-563">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="32d0b-563">PENSION</span></span>                | <span data-ttu-id="32d0b-564">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="32d0b-564">Pension</span></span>                        | <span data-ttu-id="32d0b-565">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-565">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-566">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-566">TERMINATION</span></span>            | <span data-ttu-id="32d0b-567">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-567">Termination</span></span>                    | <span data-ttu-id="32d0b-568">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-568">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-569">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-569">RETIREMENT</span></span>             | <span data-ttu-id="32d0b-570">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-570">Retirement</span></span>                     | <span data-ttu-id="32d0b-571">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-571">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-572">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-572">ABSENTEE</span></span>               | <span data-ttu-id="32d0b-573">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-573">Absentee</span></span>                       | <span data-ttu-id="32d0b-574">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-574">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-575">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-575">OTHER</span></span>                  | <span data-ttu-id="32d0b-576">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-576">Other Reasons</span></span>                  | <span data-ttu-id="32d0b-577">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-577">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-578">การปิด</span><span class="sxs-lookup"><span data-stu-id="32d0b-578">CLOSURE</span></span>                | <span data-ttu-id="32d0b-579">การปิดของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="32d0b-579">Business Closure</span></span>               | <span data-ttu-id="32d0b-580">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-580">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-581">ความตาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-581">DEATH</span></span>                  | <span data-ttu-id="32d0b-582">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="32d0b-582">Death</span></span>                          | <span data-ttu-id="32d0b-583">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-583">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="32d0b-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="32d0b-585">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="32d0b-585">Leave of Absence</span></span>               | <span data-ttu-id="32d0b-586">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-586">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="32d0b-587">CONTRACTEND</span></span>            | <span data-ttu-id="32d0b-588">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="32d0b-588">End of Contract</span></span>                | <span data-ttu-id="32d0b-589">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-589">Terminate worker</span></span>     |
| <span data-ttu-id="32d0b-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="32d0b-590">SALARYCHANGE</span></span>           | <span data-ttu-id="32d0b-591">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="32d0b-591">Change of Salary</span></span>               | <span data-ttu-id="32d0b-592">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="32d0b-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="32d0b-593">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-593">Terms of employment</span></span>

<span data-ttu-id="32d0b-594">มีการใช้เงื่อนไขของการจ้างงาน เพื่อสร้างประเภทและตัวอย่างของการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="32d0b-595">เงื่อนไขถูกแม็ปกับ Dayforce เป็นค่าตัวบ่งชี้การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="32d0b-596">เงื่อนไขการจ้างงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="32d0b-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="32d0b-597">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-597">Terms of employment</span></span>   | <span data-ttu-id="32d0b-598">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="32d0b-599">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="32d0b-599">Regular</span></span>               | <span data-ttu-id="32d0b-600">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="32d0b-600">Regular</span></span>     |
| <span data-ttu-id="32d0b-601">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="32d0b-601">Direct</span></span>                | <span data-ttu-id="32d0b-602">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="32d0b-602">Direct</span></span>      |
| <span data-ttu-id="32d0b-603">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-603">Internship</span></span>            | <span data-ttu-id="32d0b-604">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-604">Internship</span></span>  |
| <span data-ttu-id="32d0b-605">ถาวร</span><span class="sxs-lookup"><span data-stu-id="32d0b-605">Permanent</span></span>             | <span data-ttu-id="32d0b-606">ถาวร</span><span class="sxs-lookup"><span data-stu-id="32d0b-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="32d0b-607">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="32d0b-607">Marital status</span></span>

<span data-ttu-id="32d0b-608">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="32d0b-609">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="32d0b-610">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-610">Talent</span></span>                 | <span data-ttu-id="32d0b-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="32d0b-612">สมรส</span><span class="sxs-lookup"><span data-stu-id="32d0b-612">Married</span></span>                | <span data-ttu-id="32d0b-613">สมรส</span><span class="sxs-lookup"><span data-stu-id="32d0b-613">Married</span></span>                   |
| <span data-ttu-id="32d0b-614">โสด</span><span class="sxs-lookup"><span data-stu-id="32d0b-614">Single</span></span>                 | <span data-ttu-id="32d0b-615">โสด</span><span class="sxs-lookup"><span data-stu-id="32d0b-615">Single</span></span>                    |
| <span data-ttu-id="32d0b-616">หม้าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-616">Widowed</span></span>                | <span data-ttu-id="32d0b-617">หม้าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-617">Widowed</span></span>                   |
| <span data-ttu-id="32d0b-618">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-618">Divorced</span></span>               | <span data-ttu-id="32d0b-619">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-619">Divorced</span></span>                  |
| <span data-ttu-id="32d0b-620">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="32d0b-620">Registered Partnership</span></span> | <span data-ttu-id="32d0b-621">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="32d0b-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="32d0b-622">None</span><span class="sxs-lookup"><span data-stu-id="32d0b-622">None</span></span>                   | <span data-ttu-id="32d0b-623">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="32d0b-624">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-624">Cohabiting</span></span>             | <span data-ttu-id="32d0b-625">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="32d0b-626">เพศ</span><span class="sxs-lookup"><span data-stu-id="32d0b-626">Gender</span></span>

<span data-ttu-id="32d0b-627">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="32d0b-628">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="32d0b-629">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-629">Talent</span></span>       | <span data-ttu-id="32d0b-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="32d0b-631">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-631">Male</span></span>         | <span data-ttu-id="32d0b-632">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="32d0b-632">Male</span></span>                      |
| <span data-ttu-id="32d0b-633">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="32d0b-633">Female</span></span>       | <span data-ttu-id="32d0b-634">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="32d0b-634">Female</span></span>                    |
| <span data-ttu-id="32d0b-635">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="32d0b-635">Non-specific</span></span> | <span data-ttu-id="32d0b-636">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="32d0b-637">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="32d0b-637">Payment method</span></span>

<span data-ttu-id="32d0b-638">วิธีการชำระเงินให้พนักงานและบริษัทมีวิธีในการอธิบายวิธีการจ่ายเงินแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="32d0b-639">วิธีการชำระเงินถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="32d0b-640">ตารางต่อไปนี้แสดงวิธีการแม็ปวิธีการชำระเงินกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="32d0b-641">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-641">Talent</span></span>             | <span data-ttu-id="32d0b-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="32d0b-643">เงินสด</span><span class="sxs-lookup"><span data-stu-id="32d0b-643">Cash</span></span>               | <span data-ttu-id="32d0b-644">เงินสด</span><span class="sxs-lookup"><span data-stu-id="32d0b-644">Cash</span></span>                      |
| <span data-ttu-id="32d0b-645">การชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="32d0b-645">Electronic Payment</span></span> | <span data-ttu-id="32d0b-646">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-646">Transfer</span></span>                  |
| <span data-ttu-id="32d0b-647">ตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="32d0b-647">Check</span></span>              | <span data-ttu-id="32d0b-648">เช็ค</span><span class="sxs-lookup"><span data-stu-id="32d0b-648">Cheque</span></span>                    |
| <span data-ttu-id="32d0b-649">ตั๋วแลกเงินธนาคาร</span><span class="sxs-lookup"><span data-stu-id="32d0b-649">Bank Draft</span></span>         | <span data-ttu-id="32d0b-650">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="32d0b-651">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="32d0b-651">Other</span></span>              | <span data-ttu-id="32d0b-652">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="32d0b-653">ชนิดของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="32d0b-653">Bank account type</span></span>

<span data-ttu-id="32d0b-654">ชนิดของบัญชีธนาคารถูกใช้สำหรับการชำระเงินทางอิเล็กทรอนิกส์แก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="32d0b-655">ชนิดบัญชีธนาคารถูกแม็ปกับ Dayforce เป็นข้อมูลบัญชีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="32d0b-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="32d0b-656">ชนิดของบัญชีธนาคารจะถูกแปล ตามความเหมาะสม กับค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="32d0b-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="32d0b-657">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-657">Talent</span></span>            | <span data-ttu-id="32d0b-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="32d0b-659">บัญชีกระแสรายวัน</span><span class="sxs-lookup"><span data-stu-id="32d0b-659">Checking Account</span></span>  | <span data-ttu-id="32d0b-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="32d0b-660">CheckingAccount</span></span>           |
| <span data-ttu-id="32d0b-661">บัญชีเครดิตค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="32d0b-661">Payroll Account</span></span>   | <span data-ttu-id="32d0b-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="32d0b-662">PayrollAccount</span></span>            |
| <span data-ttu-id="32d0b-663">บัญชีออมทรัพย์</span><span class="sxs-lookup"><span data-stu-id="32d0b-663">Savings Account</span></span>   | <span data-ttu-id="32d0b-664">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="32d0b-665">บัญชี BankGirot</span><span class="sxs-lookup"><span data-stu-id="32d0b-665">BankGirot account</span></span> | <span data-ttu-id="32d0b-666">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="32d0b-667">บัญชี PlusGirot</span><span class="sxs-lookup"><span data-stu-id="32d0b-667">PlusGirot account</span></span> | <span data-ttu-id="32d0b-668">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="32d0b-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="32d0b-669">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-669">Earning codes</span></span>

<span data-ttu-id="32d0b-670">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="32d0b-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="32d0b-671">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="32d0b-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="32d0b-672">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="32d0b-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="32d0b-673">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="32d0b-673">Supported frequencies</span></span>

- <span data-ttu-id="32d0b-674">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="32d0b-674">All</span></span>
- <span data-ttu-id="32d0b-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="32d0b-675">EVERYPAY</span></span>
- <span data-ttu-id="32d0b-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="32d0b-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="32d0b-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="32d0b-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="32d0b-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="32d0b-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="32d0b-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-679">1OFMTH</span></span>
- <span data-ttu-id="32d0b-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-680">LASTOFMTH</span></span>
- <span data-ttu-id="32d0b-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-681">2OFMTH</span></span>
- <span data-ttu-id="32d0b-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-682">3OFMTH</span></span>
- <span data-ttu-id="32d0b-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-683">4OFMTH</span></span>
- <span data-ttu-id="32d0b-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-684">5OFMTH</span></span>
- <span data-ttu-id="32d0b-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-685">1N2OFMTH</span></span>
- <span data-ttu-id="32d0b-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-686">3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-687">1N3OFMTH</span></span>
- <span data-ttu-id="32d0b-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-688">1N4OFMTH</span></span>
- <span data-ttu-id="32d0b-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-689">2N3OFMTH</span></span>
- <span data-ttu-id="32d0b-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-690">2N4OFMTH</span></span>
- <span data-ttu-id="32d0b-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="32d0b-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="32d0b-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="32d0b-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="32d0b-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="32d0b-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="32d0b-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="32d0b-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="32d0b-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="32d0b-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="32d0b-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="32d0b-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="32d0b-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="32d0b-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="32d0b-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="32d0b-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="32d0b-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="32d0b-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="32d0b-703">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="32d0b-703">Addresses</span></span>

<span data-ttu-id="32d0b-704">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="32d0b-705">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="32d0b-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="32d0b-706">Talent</span><span class="sxs-lookup"><span data-stu-id="32d0b-706">Talent</span></span>              | <span data-ttu-id="32d0b-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="32d0b-708">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="32d0b-708">Country/Region</span></span>      | <span data-ttu-id="32d0b-709">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="32d0b-709">Country Code</span></span>          |
| <span data-ttu-id="32d0b-710">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="32d0b-710">Zip/Postal Code</span></span>     | <span data-ttu-id="32d0b-711">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="32d0b-711">Postal Code</span></span>           |
| <span data-ttu-id="32d0b-712">สถานะ</span><span class="sxs-lookup"><span data-stu-id="32d0b-712">State</span></span>               | <span data-ttu-id="32d0b-713">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="32d0b-713">State Code</span></span>            |
| <span data-ttu-id="32d0b-714">เมือง</span><span class="sxs-lookup"><span data-stu-id="32d0b-714">City</span></span>                | <span data-ttu-id="32d0b-715">เมือง</span><span class="sxs-lookup"><span data-stu-id="32d0b-715">City</span></span>                  |
| <span data-ttu-id="32d0b-716">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="32d0b-716">County</span></span>              | <span data-ttu-id="32d0b-717">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="32d0b-717">County (Municipality)</span></span> |
| <span data-ttu-id="32d0b-718">ถนน</span><span class="sxs-lookup"><span data-stu-id="32d0b-718">Street</span></span>              | <span data-ttu-id="32d0b-719">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="32d0b-719">Address Line 1</span></span>        |
| <span data-ttu-id="32d0b-720">หมายเลขถนน</span><span class="sxs-lookup"><span data-stu-id="32d0b-720">Street Number</span></span>       | <span data-ttu-id="32d0b-721">ที่อยู่ บรรทัดที่ 2</span><span class="sxs-lookup"><span data-stu-id="32d0b-721">Address Line 2</span></span>        |
| <span data-ttu-id="32d0b-722">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="32d0b-722">Building Complement</span></span> | <span data-ttu-id="32d0b-723">ที่อยู่ บรรทัดที่ 5</span><span class="sxs-lookup"><span data-stu-id="32d0b-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="32d0b-724">หมายเลขหนังสือเดินทาง</span><span class="sxs-lookup"><span data-stu-id="32d0b-724">Passport number</span></span>

<span data-ttu-id="32d0b-725">พนักงานสามารถประกาศข้อมูลหนังสือเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="32d0b-725">Employees can declare passport information.</span></span> <span data-ttu-id="32d0b-726">ข้อมูลนี้เป็นชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง** และถูกรวมอยู่ใน Dayforce เป็นส่วนหนึ่งของข้อมูลเม็กซิโกเฉพาะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="32d0b-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="32d0b-727">ชนิดการระบุรหัสประจำตัว = "หนังสือเดินทาง"</span><span class="sxs-lookup"><span data-stu-id="32d0b-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="32d0b-728">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="32d0b-728">Issued Date</span></span>
- <span data-ttu-id="32d0b-729">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="32d0b-729">Expiration Date</span></span>

<span data-ttu-id="32d0b-730">พนักงานสามารถประกาศหมายเลขรหัสหลายเลขของชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="32d0b-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="32d0b-731">อย่างไรก็ตาม เฉพาะรายการหนังสือเดินทางที่ใช้งานปัจจุบันจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="32d0b-732">ถ้ารายการหนังสือเดินทางทั้งหมดหมดอายุ หนังสือเดินทางที่ออกครั้งล่าสุดจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="32d0b-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

