---
title: ตั้งค่าคอนฟิกการรวมค่าจ้างระหว่าง Talent และ Dayforce
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการรวมระหว่าง Microsoft Dynamics 365 for Talent และ Ceridian Dayforce เพื่อให้คุณสามารถประมวลผลการรันค่าจ้าง
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
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
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/26/2019
ms.locfileid: "898455"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="1c73b-103">ตั้งค่าคอนฟิกการรวมระบบค่าจ้างระหว่าง Talent และ Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c73b-104">การรวมระหว่าง Microsoft Dynamics 365 for Talent และ Ceridian Dayforce ขึ้นอยู่กับขั้นตอนการตั้งค่าคอนฟิกหลายขั้นตอนที่ถูกอธิบายไว้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="1c73b-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="1c73b-105">คุณต้องตั้งค่าคอนฟิกการรวมทั้ง Talent และ Dayforce ก่อนที่คุณจะสามารถประมวลผลการชำระค่าจ้างที่รันได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="1c73b-106">เมื่อคุณใช้บริการเช่น Dayforce เพื่อทำให้การชำระค่าจ้างเสร็จสมบูรณ์ คุณต้องเปิดใช้งานการรวมใน Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="1c73b-107">การรวมจำเป็นต้องมีข้อมูลที่เฉพาะเจาะจงจาก Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="1c73b-108">ดังนั้น คุณต้องตรวจสอบว่า ข้อมูลที่มีการแม็ปกับ Dayforce ถูกตั้งค่าคอนฟิกใน Talent ในลักษณะที่สนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="1c73b-109">การรวมใช้ประเภทที่กว้างของข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="1c73b-110">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="1c73b-110">Human resources data</span></span>
- <span data-ttu-id="1c73b-111">ข้อมูลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-111">Compensation data</span></span>
- <span data-ttu-id="1c73b-112">ข้อมูลค่าจ้าง เช่น รอบการชำระค่าจ้าง รอบระยะเวลาการชำระค่าจ้าง และรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="1c73b-113">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-113">Worker data</span></span>

<span data-ttu-id="1c73b-114">หัวข้อนี้อธิบายขั้นตอนต่างๆ ที่คุณต้องปฏิบัติตามเพื่อเปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="1c73b-115">นอกจากนี้ ยังอธิบายถึงชนิดของข้อมูลและรายละเอียดการตั้งค่าคอนฟิกที่การรวมต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="1c73b-116">เปิดใช้งานการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-116">Enable the integration</span></span>

<span data-ttu-id="1c73b-117">ใน Talent คุณต้องเปิดใช้งานการรวม และป้อนข้อมูลการตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="1c73b-118">ถ้าคุณต้องการธุรกรรมบัญชีแยกประเภททั่วไปที่ถูกผลิตให้ถูกนำเข้าลงใน Microsoft Dynamics 365 for Finance and Operations คุณยังต้องตั้งค่าบัญชีที่จัดเก็บ Microsoft Azure และป้อนสตริงการเชื่อมต่อที่จัดเก็บ Azure ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1c73b-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="1c73b-119">เมื่อต้องการเปิดใช้งานการรวมใน Talent ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="1c73b-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="1c73b-120">ในหน้า **การดูแลระบบ** เลือก **การตั้งค่าคอนฟิกการรวม**</span><span class="sxs-lookup"><span data-stu-id="1c73b-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="1c73b-121">ป้อนปลายทาง File Transfer Protocol (FTP) แบบปลอดภัย และพาธโฟลเดอร์ FTP แบบปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="1c73b-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="1c73b-122">ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่จะเข้าถึงปลายทาง FTP แบบปลอดภัย และโฟลเดอร์พาธ</span><span class="sxs-lookup"><span data-stu-id="1c73b-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="1c73b-123">ทดสอบการเชื่อมต่อ หากจำเป็น และตั้งค่าตัวเลือก **เปิดใช้งานการรวมค่าจ้าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="1c73b-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="1c73b-124">เมื่อเปิดการรวม มีการสร้างแพคเกจการส่งออกข้อมูลและไฟล์ และมีการตั้งค่าความถี่</span><span class="sxs-lookup"><span data-stu-id="1c73b-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="1c73b-125">คุณสามารถเปลี่ยนความถี่นี้ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="1c73b-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบัญชีการจัดเก็บ Azure และสตริงการเชื่อมต่อการจัดเก็บ Azure ดูหัวข้อ Azure ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="1c73b-127">เกี่ยวกับบัญชีการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="1c73b-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="1c73b-128">ตั้งค่าคอนฟิกสตริงการเชื่อมต่อการจัดเก็บ Azure</span><span class="sxs-lookup"><span data-stu-id="1c73b-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="1c73b-129">ตั้งค่าคอนฟิกข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-129">Configure your data</span></span> 

<span data-ttu-id="1c73b-130">ในการประมวลผลค่าจ้าง คุณต้องตั้งค่าคอนฟิกข้อมูลทรัพยากรบุคคลใน Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="1c73b-131">คุณต้องตั้งค่าข้อมูลองค์กร เช่น งาน และตำแหน่ง พร้อมด้วยข้อมูลค่าตอบแทนและสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="1c73b-132">ข้อมูลนี้ให้ข้อมูลการจ้างงาน ค่าจ้าง และการหักลด ที่จำเป็นในการสร้างค่าจ้างของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="1c73b-133">ข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="1c73b-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="1c73b-134">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-134">Benefits</span></span> 

<span data-ttu-id="1c73b-135">ทรัพยากรบุคคลให้เครื่องมือสำหรับการตั้งค่าและการบำรุงรักษาของสวัสดิการ การหักลด และแผนค่าตอบแทนของผู้ปฏิบัติงาน ที่หน่วยงานนำเสนอหรือประมวลผลสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="1c73b-136">เมื่อคุณสร้างสวัสดิการ พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="1c73b-137">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-137">Benefit plans</span></span>

- <span data-ttu-id="1c73b-138">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-138">Plan (required)</span></span>
- <span data-ttu-id="1c73b-139">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-139">Type (required)</span></span>
- <span data-ttu-id="1c73b-140">ผลกระทบของค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-140">Payroll impact (required)</span></span>
- <span data-ttu-id="1c73b-141">ขอคืนเงินค้างชำระ</span><span class="sxs-lookup"><span data-stu-id="1c73b-141">Recover arrears</span></span>
- <span data-ttu-id="1c73b-142">วิธีการหักลด</span><span class="sxs-lookup"><span data-stu-id="1c73b-142">Deduction method</span></span>
- <span data-ttu-id="1c73b-143">ระดับความสำคัญการหักลด</span><span class="sxs-lookup"><span data-stu-id="1c73b-143">Deduction priority</span></span>
- <span data-ttu-id="1c73b-144">จำกัดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="1c73b-144">Limit period</span></span>
- <span data-ttu-id="1c73b-145">ยอดวงเงิน</span><span class="sxs-lookup"><span data-stu-id="1c73b-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="1c73b-146">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-146">Benefits</span></span>

- <span data-ttu-id="1c73b-147">แผน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-147">Plan (required)</span></span>
- <span data-ttu-id="1c73b-148">ชนิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-148">Type (required)</span></span>
- <span data-ttu-id="1c73b-149">ตัวเลือก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-149">Option (required)</span></span>
- <span data-ttu-id="1c73b-150">รหัสสวัสดิการ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-150">Benefit ID (required)</span></span>
- <span data-ttu-id="1c73b-151">ความถี่</span><span class="sxs-lookup"><span data-stu-id="1c73b-151">Frequency</span></span>
- <span data-ttu-id="1c73b-152">ข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-152">Basis</span></span>
- <span data-ttu-id="1c73b-153">ยอดเงินหรืออัตรา</span><span class="sxs-lookup"><span data-stu-id="1c73b-153">Amount or rate</span></span>
- <span data-ttu-id="1c73b-154">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="1c73b-155">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="1c73b-155">Supported frequencies</span></span> 

- <span data-ttu-id="1c73b-156">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="1c73b-156">Weekly</span></span>
- <span data-ttu-id="1c73b-157">ทุกสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="1c73b-157">Bi-weekly</span></span>
- <span data-ttu-id="1c73b-158">รายครึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-158">Semi-monthly</span></span>
- <span data-ttu-id="1c73b-159">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="1c73b-160">ฐานที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="1c73b-160">Supported bases</span></span> 

- <span data-ttu-id="1c73b-161">ยอดเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-161">Fixed amount</span></span>
- <span data-ttu-id="1c73b-162">เปอร์เซ็นต์ของรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-162">Percent of earnings</span></span>
- <span data-ttu-id="1c73b-163">ชั่วโมงที่มีประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-163">Productive hours</span></span>

<span data-ttu-id="1c73b-164">Dayforce สร้างการหักลดต่อไปนี้ โดยขึ้นอยู่กับผลกระทบของค่าจ้างที่กำหนดในแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="1c73b-165">การเลือกใน Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-165">Selection in Talent</span></span>        | <span data-ttu-id="1c73b-166">ผลลัพธ์ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="1c73b-167">None</span><span class="sxs-lookup"><span data-stu-id="1c73b-167">None</span></span>                       | <span data-ttu-id="1c73b-168">ไม่มีการสร้างการหักลด</span><span class="sxs-lookup"><span data-stu-id="1c73b-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="1c73b-169">การหักลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-169">Deduction only</span></span>             | <span data-ttu-id="1c73b-170">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="1c73b-171">การจ่ายเงินสมทบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-171">Contribution only</span></span>          | <span data-ttu-id="1c73b-172">การหักลดพนักงานจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="1c73b-173">การหักลดและการจ่ายเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="1c73b-173">Deduction and contribution</span></span> | <span data-ttu-id="1c73b-174">การหักลดพนักงานและนายจ้างจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="1c73b-175">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนด และจัดการโปรแกรมสวัสดิการ ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="1c73b-176">นำเสนอโปรแกรมสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="1c73b-177">สร้างสวัสดิการใหม่</span><span class="sxs-lookup"><span data-stu-id="1c73b-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="1c73b-178">กำหนดกฎและนโยบายการมีสิทธิ์ของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="1c73b-179">ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="1c73b-180">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-180">Compensation</span></span> 

<span data-ttu-id="1c73b-181">การจัดการค่าตอบแทนจะใช้ควบคุมการจัดส่งของค่าจ้างพื้นฐานและเงินรางวัล</span><span class="sxs-lookup"><span data-stu-id="1c73b-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="1c73b-182">ค่าจ้างพื้นฐานคงที่ของพนักงานและการขึ้นค่าตอบแทนตามผลงานจะถูกควบคุมโดยใช้แผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="1c73b-183">ค่าจ้างจูงใจเช่นการชำระเงินโบนัส รางวัลตามผลการปฏิบัติงาน สิทธิในการซื้อหุ้น การให้หุ้น รางวัลที่จ่ายครั้งเดียว โดยใช้แผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="1c73b-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="1c73b-184">Dayforce ใช้ข้อมูลค่าตอบแทนที่คำนวณอัตรารายชั่วโมงหรือรายปีของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="1c73b-185">จำเป็นต้องมีแผนค่าตอบแทนคงที่และการแปลงอัตราค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="1c73b-186">พนักงานต้องเชื่อมโยงกับแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="1c73b-187">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแผนค่าตอบแทน โปรดดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="1c73b-188">สร้างแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="1c73b-189">สร้างแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="1c73b-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="1c73b-190">พัฒนาโครงสร้างและแผนเงินเดือน/ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="1c73b-191">ประมวลผลค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="1c73b-192">กำหนดกระบวนการของค่าตอบแทนและคำนวณผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="1c73b-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="1c73b-193">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="1c73b-194">การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="1c73b-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="1c73b-195">งาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-195">Jobs</span></span> 

<span data-ttu-id="1c73b-196">งานเป็นชุดของงานและความรับผิดชอบที่ถูกระบุของบุคคลที่ดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="1c73b-197">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1c73b-198">การตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="1c73b-199">กำหนดงานใหม่</span><span class="sxs-lookup"><span data-stu-id="1c73b-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="1c73b-200">ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1c73b-200">Positions</span></span>

<span data-ttu-id="1c73b-201">ตำแหน่งคือแต่ละอินสแตนซ์ของงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="1c73b-202">ตัวอย่างเช่น ตำแหน่ง "ผู้จัดการฝ่ายขาย (ตะวันออก)" เป็นหนึ่งในตำแหน่งที่เชื่อมโยงกับงาน "ผู้จัดการฝ่ายขาย"</span><span class="sxs-lookup"><span data-stu-id="1c73b-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="1c73b-203">ตำแหน่งมีอยู่ในแผนก</span><span class="sxs-lookup"><span data-stu-id="1c73b-203">A position exists in a department.</span></span> <span data-ttu-id="1c73b-204">สามารถเชื่อมโยงผู้ปฏิบัติงานหนึ่งรายกับแต่ละตำแหน่งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="1c73b-205">เก็บข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ไว้ เมื่อคุณตั้งค่าตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="1c73b-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="1c73b-206">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-206">Position (required)</span></span>
- <span data-ttu-id="1c73b-207">คำอธิบาย (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-207">Description (required)</span></span>
- <span data-ttu-id="1c73b-208">งาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-208">Job (required)</span></span>
- <span data-ttu-id="1c73b-209">แผนก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-209">Department (required)</span></span>
- <span data-ttu-id="1c73b-210">ชนิดตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-210">Position type (required)</span></span>
- <span data-ttu-id="1c73b-211">จำนวนบุคลากรเทียบเท่าเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="1c73b-211">Full-time equivalent</span></span>
- <span data-ttu-id="1c73b-212">ชั่วโมงปกติรายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="1c73b-213">ชำระโดยนิติบุคคล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="1c73b-214">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-214">Pay cycle (required)</span></span>
- <span data-ttu-id="1c73b-215">มิติทางการเงินเริ่มต้น – ศูนย์ต้นทุน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="1c73b-216">การมอบหมายผู้ปฏิบัติงาน – ผู้ปฏิบัติงาน การเริ่มต้นการกำหนด การสิ้นสุดการกำหนด รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="1c73b-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="1c73b-217">ถ้าตำแหน่งหลายตำแหน่งในแผนกเดียวกันเกี่ยวข้องกับงานเดียวกัน จะมีการรวมลงในตำแหน่งหนึ่งๆ ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="1c73b-218">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1c73b-219">จัดระเบียบบุคลากรของคุณโดยใช้แผนก งาน และตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1c73b-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="1c73b-220">ตั้งค่าตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1c73b-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="1c73b-221">แผนก</span><span class="sxs-lookup"><span data-stu-id="1c73b-221">Departments</span></span>

<span data-ttu-id="1c73b-222">แผนกเป็นหน่วยปฏิบัติงานที่แสดงถึงประเภทหรือพื้นที่ทำงานขององค์กร</span><span class="sxs-lookup"><span data-stu-id="1c73b-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="1c73b-223">แผนกจะรับผิดชอบพื้นที่เฉพาะขององค์กร เช่น การขาย การบัญชี หรือทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="1c73b-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="1c73b-224">คุณสามารถใช้แผนกต่างๆเพื่อรายงานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="1c73b-225">แผนกอาจมีความรับผิดชอบกำไรและขาดทุน</span><span class="sxs-lookup"><span data-stu-id="1c73b-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="1c73b-226">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1c73b-227">สร้างแผนกและการเชื่อมโยงกับลำดับชั้นของแผนก</span><span class="sxs-lookup"><span data-stu-id="1c73b-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="1c73b-228">กำหนดฝ่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="1c73b-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="1c73b-229">รอบการชำระค่าจ้างและรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="1c73b-230">รอบการชำระค่าจ้างกำหนดความถี่ในการรันค่าจ้าง และจำนวนวันที่เจาะจงเมื่อผู้ปฏิบัติงานได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="1c73b-231">ตัวอย่างเช่น รอบการชำระค่าจ้างอาจเป็นรายเดือน และพนักงานอาจได้รับค่าจ้างในวันสุดท้ายของเดือนนั้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="1c73b-232">อีกทางหนึ่งคือ รอบการชำระค่าจ้างอาจเป็นรายสัปดาห์ และพนักงานอาจได้รับค่าจ้างในวันอังคารหลังจากจุดสิ้นสุดของรอบระยะเวลาการชำระค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="1c73b-233">รอบการชำระค่าจ้างถูกกำหนดให้กับตำแหน่ง เพื่อควบคุมเวลาที่ผู้ปฏิบัติงานในตำแหน่งเหล่านั้นได้รับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="1c73b-234">หลังจากที่คุณสร้างรอบการชำระค่าจ้าง คุณสามารถสร้างรอบระยะเวลาการชำระค่าจ้างสำหรับแต่ละรอบได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="1c73b-235">รอบการชำระค่าจ้างแต่ละรอบรวมถึงวันที่ของการชำระเงินเริ่มต้นที่ยึดตามข้อมูลที่คุณให้</span><span class="sxs-lookup"><span data-stu-id="1c73b-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="1c73b-236">อย่างไรก็ตาม คุณสามารถแก้ไขวันที่การชำระเงินเริ่มต้นได้ในรอบการชำระค่าจ้างเพื่อให้อนุญาตการยกเว้น เช่น เมื่อวันที่ชำระเงินตรงกับวันหยุด</span><span class="sxs-lookup"><span data-stu-id="1c73b-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="1c73b-237">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="1c73b-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="1c73b-238">รอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-238">Pay cycle (required)</span></span>
- <span data-ttu-id="1c73b-239">ความถี่ของรอบการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="1c73b-240">วันที่เริ่มรอบระยะเวลา (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="1c73b-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="1c73b-241">วันที่การชำระเงินเริ่มต้น (รอบการชำระค่าจ้างแรกที่ต้องการ)</span><span class="sxs-lookup"><span data-stu-id="1c73b-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="1c73b-242">ข้อมูลนี้ถูกรวมเข้ากับ Dayforce เป็นกลุ่มค่าจ้าง และจะถูกแยกตามประเทศหรือภูมิภาคสำหรับรอบการชำระค่าจ้างแต่ละรอบ</span><span class="sxs-lookup"><span data-stu-id="1c73b-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="1c73b-243">ต้องมีการสร้างรอบระยะเวลาการชำระค่าจ้างอย่างน้อยหนึ่งรายการ ก่อนที่จะรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="1c73b-244">Dayforce สร้างปฏิทินกลุ่มค่าจ้างและวันที่ในการชำระเงิน โดยยึดตามวันที่เริ่มต้นของรอบระยะเวลาการชำระค่าจ้างแรก และวันที่ชำระเงินเริ่มต้นที่ตั้งค่าใน Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="1c73b-245">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-245">Earning codes</span></span>

<span data-ttu-id="1c73b-246">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="1c73b-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1c73b-247">รหัสมีพารามิเตอร์ต่าง ๆ ที่เกี่ยวข้องกับรายได้ เช่น แต่ละ กฎทางบัญชี กฎภาษี และรายงานความต้องการและความสามารถในการรวมได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="1c73b-248">มีการใช้ข้อมูลต่อไปนี้ใน Dayforce:</span><span class="sxs-lookup"><span data-stu-id="1c73b-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="1c73b-249">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-249">Earning Code (required)</span></span>
- <span data-ttu-id="1c73b-250">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-250">Description</span></span>
- <span data-ttu-id="1c73b-251">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="1c73b-251">Unit of measure</span></span>
- <span data-ttu-id="1c73b-252">ประสิทธิผลการทำงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="1c73b-253">ข้อมูลของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-253">Worker data</span></span>

<span data-ttu-id="1c73b-254">เรกคอร์ดสำหรับชนิดต่างๆ ของผู้ปฏิบัติงานที่คุณมี มีความสำคัญสำหรับระบบค่าจ้างและทรัพยากรบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="1c73b-255">ข้อมูลที่คุณป้อนสามารถใช้ติดตามผู้ปฏิบัติงานและข้อมูลส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="1c73b-256">คุณสามารถรักษาข้อมูลต่อไปนี้สำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="1c73b-257">**พื้นฐาน** – รักษาข้อมูลพื้นฐานเกี่ยวกับผู้ปฏิบัติงาน เช่น ข้อมูลการติดต่อ ข้อมูลทางประชากรศาสตร์ ข้อมูลการระบุรหัสประจำตัว ข้อมูลครอบครัว สถานะการรับราชการทหาร ข้อมูลคนต่างด้าว และผู้ติดต่อได้ในกรณีฉุกเฉินและส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="1c73b-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="1c73b-258">**การจ้างงาน** – รักษาข้อมูลเกี่ยวกับการจ้างงานของผู้ปฏิบัติงาน เช่น บริษัท หรือสังกัดองค์กร การมอบหมายตำแหน่งงาน วันที่เริ่มต้นและสิ้นสุด สิทธิการทำงาน เงื่อนไขในการจ้างงาน เงินบำนาญ วันหยุดพักผ่อน และข้อมูลการย้ายสถานที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="1c73b-259">**การลางานและการขาดงาน** – รักษาข้อมูลเกี่ยวกับการขาดงานของผู้ปฏิบัติงาน เช่น ปฏิทินการทำงาน ธุรกรรมการขาดงาน และการตั้งค่าการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="1c73b-260">**ค่าตอบแทนและค่าจ้าง** – รักษาข้อมูลเกี่ยวกับแผนค่าตอบแทนของผู้ปฏิบัติงานและข้อมูลค่าจ้าง เช่น การลงทะเบียนสำหรับแผน รางวัล ประสิทธิภาพ ค่าคอมมิชชัน ข้อมูลภาษี การเกษียณอายุ และการหักเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="1c73b-261">เมื่อคุณป้อนข้อมูลผู้ปฏิบัติงาน พึงระลึกว่าข้อมูลและการตั้งค่าคอนฟิกต่อไปนี้ที่ใช้ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="1c73b-262">ข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="1c73b-262">General information</span></span>

- <span data-ttu-id="1c73b-263">หมายเลขบุคลากร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-263">Personnel number (required)</span></span>
- <span data-ttu-id="1c73b-264">ชื่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-264">First name (required)</span></span>
- <span data-ttu-id="1c73b-265">นามสกุล (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-265">Last name (required)</span></span>
- <span data-ttu-id="1c73b-266">ชื่อกลาง</span><span class="sxs-lookup"><span data-stu-id="1c73b-266">Middle name</span></span>
- <span data-ttu-id="1c73b-267">วันที่ของอายุงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-267">Seniority date</span></span>
- <span data-ttu-id="1c73b-268">เรียกว่า</span><span class="sxs-lookup"><span data-stu-id="1c73b-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="1c73b-269">ข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="1c73b-269">Personal information</span></span>

- <span data-ttu-id="1c73b-270">สถานภาพการสมรส (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-270">Marital status (required)</span></span>
- <span data-ttu-id="1c73b-271">วันที่เกิด (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-271">Birth date (required)</span></span>
- <span data-ttu-id="1c73b-272">เพศ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-272">Gender (required)</span></span>
- <span data-ttu-id="1c73b-273">บุคคลทุพพลภาพ</span><span class="sxs-lookup"><span data-stu-id="1c73b-273">Person with disabilities</span></span>
- <span data-ttu-id="1c73b-274">สัญชาติประเทศภูมิภาค (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="1c73b-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="1c73b-275">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="1c73b-275">Address information</span></span>

- <span data-ttu-id="1c73b-276">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-276">Primary (required)</span></span>
- <span data-ttu-id="1c73b-277">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-277">Country/region (required)</span></span>
- <span data-ttu-id="1c73b-278">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-278">Postal code (required)</span></span>
- <span data-ttu-id="1c73b-279">หมายเลขถนน (จำเป็น) (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="1c73b-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="1c73b-280">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร (เฉพาะสำหรับเม็กซิโก)</span><span class="sxs-lookup"><span data-stu-id="1c73b-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="1c73b-281">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-281">City (required)</span></span>
- <span data-ttu-id="1c73b-282">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-282">State (required)</span></span>
- <span data-ttu-id="1c73b-283">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="1c73b-284">ข้อมูลการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="1c73b-284">Contact information</span></span> 

- <span data-ttu-id="1c73b-285">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-285">Primary (required)</span></span>
- <span data-ttu-id="1c73b-286">หมายเลขผู้ติดต่อ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-286">Contact number (required)</span></span>
- <span data-ttu-id="1c73b-287">การขยาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="1c73b-288">ข้อมูลค่าจ้างและรหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-288">Payroll information and earning codes</span></span>

<span data-ttu-id="1c73b-289">พนักงานอาจถูกกำหนดรายได้เฉพาะที่ความถี่ที่กำหนดของการชำระเงิน และมีวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="1c73b-290">ฟิลด์ต่อไปนี้จะใช้ใน Dayforce เพื่อช่วยในการรับประกันว่า การกำหนดลักษณะและการตั้งค่าเหล่านั้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="1c73b-291">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-291">Earning codes</span></span>

- <span data-ttu-id="1c73b-292">ตำแหน่ง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-292">Position (required)</span></span>
- <span data-ttu-id="1c73b-293">รหัสรายได้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-293">Earning Code (required)</span></span>
- <span data-ttu-id="1c73b-294">ความถี่ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-294">Frequency (required)</span></span>
- <span data-ttu-id="1c73b-295">จำนวน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="1c73b-296">ข้อมูลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-296">Payroll information</span></span>

- <span data-ttu-id="1c73b-297">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1c73b-297">Payment Method</span></span>
- <span data-ttu-id="1c73b-298">ภูมิภาคเศรษฐกิจ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-298">Economic Region (required)</span></span>
- <span data-ttu-id="1c73b-299">รหัสสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-299">Employee Benefits ID</span></span>
- <span data-ttu-id="1c73b-300">หมายเลขรหัสประจำชาติ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-300">National ID Number (required)</span></span>
- <span data-ttu-id="1c73b-301">หมายเลขการรับราชการทหาร</span><span class="sxs-lookup"><span data-stu-id="1c73b-301">Military Service Number</span></span>
- <span data-ttu-id="1c73b-302">รหัสกะ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-302">Shift ID (required)</span></span>
- <span data-ttu-id="1c73b-303">หมายเลขภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-303">Tax Number (required)</span></span>
- <span data-ttu-id="1c73b-304">รหัสสหภาพ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-304">Union ID (required)</span></span>
- <span data-ttu-id="1c73b-305">รหัสวันทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-305">Work Day ID (required)</span></span>
- <span data-ttu-id="1c73b-306">หมายเลขใบอนุญาตทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="1c73b-307">สำหรับวิธีการชำระเงิน เม็กซิโกสนับสนุน **เงินสด** **เช็ค** (เช็คจริงของบริษัท) และ **การชำระเงินทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="1c73b-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="1c73b-308">ถ้าไม่มีการระบุวิธีการชำระเงิน **เช็ค** จะถูกใช้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="1c73b-309">รายละเอียดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-309">Employment details</span></span>

<span data-ttu-id="1c73b-310">ประวัติรายละเอียดตการจ้างงานถูกใช้เป็นข้อมูลสำคัญในการสืบทอดการพนักงานจ้างงานของพนักงาน การหยุดชะงัก และสถานะการจ้างงานใหม่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="1c73b-311">Dayforce สนับสนุนเรกคอร์ดการจ้างงานที่ใช้งานอยู่เพียงรายการเดียวในแต่ละครั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="1c73b-312">วันที่เริ่มต้นการจ้างงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-312">Employment start date (required)</span></span>
- <span data-ttu-id="1c73b-313">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-313">Employment end date</span></span>
- <span data-ttu-id="1c73b-314">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-314">Start date</span></span>
- <span data-ttu-id="1c73b-315">วันที่เริ่มต้นที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="1c73b-315">Adjusted start date</span></span>
- <span data-ttu-id="1c73b-316">วันที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="1c73b-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="1c73b-317">เหตุผลที่สิ้นสุด (จำเป็นเมื่อสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="1c73b-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="1c73b-318">วันสำคัญของพนักงานได้รับมาโดยใช้ข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1c73b-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="1c73b-319">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-319">Talent</span></span>                | <span data-ttu-id="1c73b-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c73b-321">วันที่จ้างงานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="1c73b-321">Most recent hire date</span></span> | <span data-ttu-id="1c73b-322">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="1c73b-323">วันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-323">Termination date</span></span>      | <span data-ttu-id="1c73b-324">วันที่สิ้นสุดการจ้างงานของเรกคอร์ดประวัติการจ้างงานที่ไม่สิ้นสุดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="1c73b-325">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-325">Start date</span></span>            | <span data-ttu-id="1c73b-326">วันที่เริ่มต้นที่ปรับปรุงแล้ว วันที่เริ่มต้น หรือการเริ่มต้นการจ้างงานของเรกคอร์ประวัติการจ้างงานที่ไม่ได้ใช้งานอยู่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="1c73b-327">วันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="1c73b-327">Original hire date</span></span>    | <span data-ttu-id="1c73b-328">การเริ่มต้นการจ้างงานของเรกคอร์ดประวัติการจ้างงานแรกสุด</span><span class="sxs-lookup"><span data-stu-id="1c73b-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="1c73b-329">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-329">Compensation</span></span>

<span data-ttu-id="1c73b-330">แผนค่าตอบแทนคงต้องเชื่อมโยงกับตำแหน่งหลักของพนักงานทุกตำแหน่ง ตลอดรอบระยะเวลาการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="1c73b-331">รอบระยะเวลานี้เริ่มต้นในวันที่ที่พนักงานถูกจ้างงาน (หรือวันที่เริ่มต้นการจ้างงาน) และดำเนินต่อไปจนกว่าจะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="1c73b-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="1c73b-332">วันที่มีผลบังคับใช้ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-332">Effective Date (required)</span></span>
- <span data-ttu-id="1c73b-333">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="1c73b-333">Expiration date</span></span>
- <span data-ttu-id="1c73b-334">อัตราการชำระค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-334">Pay Rate (required)</span></span>
- <span data-ttu-id="1c73b-335">การแปลงอัตราค่าจ้าง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="1c73b-336">จำนวนเทียบเท่ารายปี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="1c73b-337">จำนวนเทียบเท่ารายชั่วโมง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="1c73b-338">ถ้าพนักงานรายชั่วโมงมีตำแหน่งหลายตำแหน่ง ค่าตอบแทนคงที่ของตำแหน่งหลักจะถูกนำเข้าใน Dayforce เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="1c73b-339">สำหรับตำแหน่งที่ไม่ใช่ตำแหน่งหลัก อัตรารายชั่วโมงถูกบันทึกลงในตำแหน่งที่สอดคล้องกันใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="1c73b-340">ถ้าพนักงานประจำมีตำแหน่งหลายตำแหน่ง จะได้รับอัตราชั่วโมงสะสมและเงินเดือนต่อปีระหว่างตำแหน่งที่ใช้งานอยู่ทั้งหมด และถูกใช้เป็นอัตรา/เงินเดือนพื้นฐานระดับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="1c73b-341">หมายเลขรหัส</span><span class="sxs-lookup"><span data-stu-id="1c73b-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="1c73b-342">ตัวระบุประกันสังคม</span><span class="sxs-lookup"><span data-stu-id="1c73b-342">Social Security identifier</span></span> 

<span data-ttu-id="1c73b-343">พนักงานทุกคนต้องมีตัวระบุหลักหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="1c73b-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="1c73b-344">ตัวระบุนี้ต้องเป็นชนิดรหัส **SSN**</span><span class="sxs-lookup"><span data-stu-id="1c73b-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="1c73b-345">ใน Dayforce จะได้รับมาโดยอัตโนมัติเป็นตัวระบุประกันสังคมของพนักงานที่จำเป็นสำหรับการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="1c73b-346">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-346">Primary (required)</span></span>
- <span data-ttu-id="1c73b-347">ชนิดข้อมูลประจำตัว = "SSN"</span><span class="sxs-lookup"><span data-stu-id="1c73b-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="1c73b-348">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="1c73b-348">Issued Date</span></span>
- <span data-ttu-id="1c73b-349">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="1c73b-349">Expiration Date</span></span>

<span data-ttu-id="1c73b-350">พนักงานสามารถประกาศหมายเลขการระบุรหัสประจำตัวหลายเลขของชนิดการระบุรหัสประจำตัว **SSN**</span><span class="sxs-lookup"><span data-stu-id="1c73b-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="1c73b-351">อย่างไรก็ตาม เฉพาะเรกคอร์ดที่ถูกทำเครื่องหมายเป็น **หลัก** ถูกรวมเข้ากับ Dayforce ไม่ว่าหมายเลขจะใช้งานอยู่ หรือหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="1c73b-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="1c73b-352">บัญชีธนาคารและการเบิกจ่าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="1c73b-353">ต้องป้อนข้อมูลบัญชีธนาคารที่ถูกต้องสำหรับพนักงานใดๆ ที่เลือกที่จะรับการชำระเงินผ่านการโอนย้ายของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1c73b-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="1c73b-354">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-354">Talent</span></span>                         | <span data-ttu-id="1c73b-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c73b-356">หมายเลขบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="1c73b-357">รหัส SWIFT (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-357">SWIFT code (required)</span></span>          | <span data-ttu-id="1c73b-358">ฟิลด์ **รหัสธนาคาร** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="1c73b-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="1c73b-359">หมายเลขสาขา (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="1c73b-360">ชนิดของบัญชีธนาคาร (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-360">Bank account type (required)</span></span>   | <span data-ttu-id="1c73b-361">ฟิลด์ **ชนิดของบัญชี** ใช้เมื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="1c73b-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="1c73b-362">ค่าที่ได้รับการสนับสนุนได้แก่ **การตรวจสอบ** และ **ค่าจ้าง**</span><span class="sxs-lookup"><span data-stu-id="1c73b-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="1c73b-363">พนักงานที่เลือกจะรับการชำระผ่านการโอนผ่านบัญชีธนาคาร ต้องมีลิงก์ไปยังบัญชีเงินส่วนที่เหลือที่อยู่ภายใต้นิติบุคคลที่มีที่อยู่หลักในเม็กซิโก และเชื่อมโยงกับบัญชีธนาคารที่ถูกต้องจากธนาคารเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="1c73b-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="1c73b-364">บัญชีที่ไม่ใช่เงินส่วนที่เหลืออื่นๆ ทั้งหมดจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="1c73b-365">รายละเอียดที่อยู่</span><span class="sxs-lookup"><span data-stu-id="1c73b-365">Address information</span></span>

<span data-ttu-id="1c73b-366">พนักงานทุกคนต้องมีสถานที่หลักหนึ่งแห่ง</span><span class="sxs-lookup"><span data-stu-id="1c73b-366">Every employee must have one primary location.</span></span> <span data-ttu-id="1c73b-367">ใน Dayforce สถานที่นี้จะใช้เพื่อกำหนดที่พักอาศัยหลักของพนักงานสำหรับวัตถุประสงค์ด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="1c73b-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="1c73b-368">หลัก (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-368">Primary (required)</span></span>
- <span data-ttu-id="1c73b-369">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-369">Country/region (required)</span></span>
- <span data-ttu-id="1c73b-370">รหัสไปรษณีย์ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="1c73b-371">ถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-371">Street (required)</span></span>
- <span data-ttu-id="1c73b-372">หมายเลขถนน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-372">Street Number (required)</span></span>
- <span data-ttu-id="1c73b-373">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="1c73b-373">Building Complement</span></span>
- <span data-ttu-id="1c73b-374">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-374">City (required)</span></span>
- <span data-ttu-id="1c73b-375">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-375">State (required)</span></span>
- <span data-ttu-id="1c73b-376">เขต (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="1c73b-377">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="1c73b-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="1c73b-378">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในสหรัฐอเมริกาและแคนาดา ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="1c73b-379">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-379">Departments are required on positions.</span></span>
- <span data-ttu-id="1c73b-380">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="1c73b-381">คุณสามารถตั้งค่าคอนฟิก Talent เพื่อกำหนดว่า ตำแหน่งต้องระบุแผนก</span><span class="sxs-lookup"><span data-stu-id="1c73b-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="1c73b-382">เมื่อต้องการทำเช่นนี้ ไปยัง **ตำแหน่งที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล > ตำแหน่ง > ต้องการแผนกในตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="1c73b-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="1c73b-383">เราขอแนะนำให้ การตั้งค่านี้ถูกบังคับใช้สำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="1c73b-384">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-384">Job types</span></span>

<span data-ttu-id="1c73b-385">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="1c73b-386">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในสหรัฐอเมริกาและแคนาดา</span><span class="sxs-lookup"><span data-stu-id="1c73b-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="1c73b-387">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1c73b-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1c73b-388">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="1c73b-389">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-390">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-390">Job type</span></span>   | <span data-ttu-id="1c73b-391">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="1c73b-392">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1c73b-392">Hourly</span></span>     | <span data-ttu-id="1c73b-393">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1c73b-393">Hourly</span></span>      |
| <span data-ttu-id="1c73b-394">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-394">Salaried</span></span>   | <span data-ttu-id="1c73b-395">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="1c73b-396">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-396">Position types</span></span> 

<span data-ttu-id="1c73b-397">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="1c73b-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="1c73b-398">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1c73b-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="1c73b-399">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-400">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1c73b-400">Position type</span></span>   | <span data-ttu-id="1c73b-401">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="1c73b-402">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="1c73b-402">Full-time</span></span>       | <span data-ttu-id="1c73b-403">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="1c73b-403">Full time employee</span></span> |
| <span data-ttu-id="1c73b-404">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1c73b-404">Part-time</span></span>       | <span data-ttu-id="1c73b-405">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1c73b-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="1c73b-406">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="1c73b-406">Reason codes</span></span>

<span data-ttu-id="1c73b-407">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="1c73b-408">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="1c73b-409">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-410">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="1c73b-410">Reason code</span></span>    | <span data-ttu-id="1c73b-411">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-411">Description</span></span>      | <span data-ttu-id="1c73b-412">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="1c73b-413">การลาออก</span><span class="sxs-lookup"><span data-stu-id="1c73b-413">RESIGNATION</span></span>    | <span data-ttu-id="1c73b-414">การลาออก</span><span class="sxs-lookup"><span data-stu-id="1c73b-414">Resignation</span></span>      | <span data-ttu-id="1c73b-415">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-415">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-416">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-416">TERMINATION</span></span>    | <span data-ttu-id="1c73b-417">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-417">Termination</span></span>      | <span data-ttu-id="1c73b-418">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-418">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-419">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-419">RETIREMENT</span></span>     | <span data-ttu-id="1c73b-420">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-420">Retirement</span></span>       | <span data-ttu-id="1c73b-421">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-421">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-422">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-422">OTHER</span></span>          | <span data-ttu-id="1c73b-423">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-423">Other Reasons</span></span>    | <span data-ttu-id="1c73b-424">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-424">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-425">ความตาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-425">DEATH</span></span>          | <span data-ttu-id="1c73b-426">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="1c73b-426">Death</span></span>            | <span data-ttu-id="1c73b-427">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-427">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="1c73b-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="1c73b-429">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="1c73b-429">Leave of Absence</span></span> | <span data-ttu-id="1c73b-430">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-430">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="1c73b-431">CONTRACTEND</span></span>    | <span data-ttu-id="1c73b-432">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="1c73b-432">End of Contract</span></span>  | <span data-ttu-id="1c73b-433">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-433">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="1c73b-434">SALARYCHANGE</span></span>   | <span data-ttu-id="1c73b-435">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-435">Change of Salary</span></span> | <span data-ttu-id="1c73b-436">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="1c73b-437">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="1c73b-437">Marital status</span></span>

<span data-ttu-id="1c73b-438">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1c73b-439">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="1c73b-440">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-440">Talent</span></span>                 | <span data-ttu-id="1c73b-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="1c73b-442">สมรส</span><span class="sxs-lookup"><span data-stu-id="1c73b-442">Married</span></span>                | <span data-ttu-id="1c73b-443">สมรส</span><span class="sxs-lookup"><span data-stu-id="1c73b-443">Married</span></span>              |
| <span data-ttu-id="1c73b-444">โสด</span><span class="sxs-lookup"><span data-stu-id="1c73b-444">Single</span></span>                 | <span data-ttu-id="1c73b-445">โสด</span><span class="sxs-lookup"><span data-stu-id="1c73b-445">Single</span></span>               |
| <span data-ttu-id="1c73b-446">หม้าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-446">Widowed</span></span>                | <span data-ttu-id="1c73b-447">หม้าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-447">Widowed</span></span>              |
| <span data-ttu-id="1c73b-448">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-448">Divorced</span></span>               | <span data-ttu-id="1c73b-449">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-449">Divorced</span></span>             |
| <span data-ttu-id="1c73b-450">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="1c73b-450">Registered Partnership</span></span> | <span data-ttu-id="1c73b-451">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="1c73b-451">Domestic Partnership</span></span> |
| <span data-ttu-id="1c73b-452">None</span><span class="sxs-lookup"><span data-stu-id="1c73b-452">None</span></span>                   | <span data-ttu-id="1c73b-453">None</span><span class="sxs-lookup"><span data-stu-id="1c73b-453">None</span></span>                 |
| <span data-ttu-id="1c73b-454">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-454">Cohabiting</span></span>             | <span data-ttu-id="1c73b-455">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="1c73b-456">เพศ</span><span class="sxs-lookup"><span data-stu-id="1c73b-456">Gender</span></span>

<span data-ttu-id="1c73b-457">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1c73b-458">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="1c73b-459">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-459">Talent</span></span>       | <span data-ttu-id="1c73b-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="1c73b-461">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-461">Male</span></span>         | <span data-ttu-id="1c73b-462">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-462">Male</span></span>            |
| <span data-ttu-id="1c73b-463">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="1c73b-463">Female</span></span>       | <span data-ttu-id="1c73b-464">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="1c73b-464">Female</span></span>          |
| <span data-ttu-id="1c73b-465">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="1c73b-465">Non-specific</span></span> | <span data-ttu-id="1c73b-466">*ไม่สนับสนุน*</span><span class="sxs-lookup"><span data-stu-id="1c73b-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="1c73b-467">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-467">Earning codes</span></span>

<span data-ttu-id="1c73b-468">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="1c73b-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1c73b-469">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1c73b-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="1c73b-470">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="1c73b-471">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="1c73b-471">Supported frequencies</span></span>

- <span data-ttu-id="1c73b-472">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1c73b-472">All</span></span>
- <span data-ttu-id="1c73b-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="1c73b-473">EVERYPAY</span></span>
- <span data-ttu-id="1c73b-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="1c73b-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="1c73b-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="1c73b-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="1c73b-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="1c73b-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="1c73b-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-477">1OFMTH</span></span>
- <span data-ttu-id="1c73b-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-478">LASTOFMTH</span></span>
- <span data-ttu-id="1c73b-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-479">2OFMTH</span></span>
- <span data-ttu-id="1c73b-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-480">3OFMTH</span></span>
- <span data-ttu-id="1c73b-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-481">4OFMTH</span></span>
- <span data-ttu-id="1c73b-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-482">5OFMTH</span></span>
- <span data-ttu-id="1c73b-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-483">1N2OFMTH</span></span>
- <span data-ttu-id="1c73b-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-484">3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-485">1N3OFMTH</span></span>
- <span data-ttu-id="1c73b-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-486">1N4OFMTH</span></span>
- <span data-ttu-id="1c73b-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-487">2N3OFMTH</span></span>
- <span data-ttu-id="1c73b-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-488">2N4OFMTH</span></span>
- <span data-ttu-id="1c73b-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="1c73b-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="1c73b-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="1c73b-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="1c73b-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="1c73b-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="1c73b-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="1c73b-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="1c73b-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="1c73b-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="1c73b-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="1c73b-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="1c73b-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1c73b-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="1c73b-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1c73b-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="1c73b-501">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="1c73b-501">Addresses</span></span>

<span data-ttu-id="1c73b-502">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="1c73b-503">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="1c73b-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="1c73b-504">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-504">Talent</span></span>          | <span data-ttu-id="1c73b-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="1c73b-506">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="1c73b-506">Country/Region</span></span>  | <span data-ttu-id="1c73b-507">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="1c73b-507">Country Code</span></span>          |
| <span data-ttu-id="1c73b-508">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="1c73b-508">Zip/Postal Code</span></span> | <span data-ttu-id="1c73b-509">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="1c73b-509">Postal Code</span></span>           |
| <span data-ttu-id="1c73b-510">สถานะ</span><span class="sxs-lookup"><span data-stu-id="1c73b-510">State</span></span>           | <span data-ttu-id="1c73b-511">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="1c73b-511">State Code</span></span>            |
| <span data-ttu-id="1c73b-512">เมือง</span><span class="sxs-lookup"><span data-stu-id="1c73b-512">City</span></span>            | <span data-ttu-id="1c73b-513">เมือง</span><span class="sxs-lookup"><span data-stu-id="1c73b-513">City</span></span>                  |
| <span data-ttu-id="1c73b-514">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="1c73b-514">County</span></span>          | <span data-ttu-id="1c73b-515">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="1c73b-515">County (Municipality)</span></span> |
| <span data-ttu-id="1c73b-516">ถนน</span><span class="sxs-lookup"><span data-stu-id="1c73b-516">Street</span></span>          | <span data-ttu-id="1c73b-517">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="1c73b-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="1c73b-518">ภูมิภาคการเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="1c73b-518">Tax regions</span></span>

<span data-ttu-id="1c73b-519">ภูมิภาคการเก็บภาษีถูกใช้เพื่อกำหนดภาษีที่เหมาะสมที่ควรนำมาใช้ในระหว่างการสร้างระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="1c73b-520">ภูมิภาคการเก็บภาษีถูกแม็ปไปยัง Dayforce เป็นที่อยู่ของสถานที่</span><span class="sxs-lookup"><span data-stu-id="1c73b-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="1c73b-521">ภูมิภาคการเก็บภาษีเริ่มต้นต้องเชื่อมโยงกับตำแหน่งงานที่ใช้งานอยู่ของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="1c73b-522">ภูมิภาคการเก็บภาษี (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-522">Tax region (required)</span></span>
- <span data-ttu-id="1c73b-523">ประเทศ/ภูมิภาค (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-523">Country/Region (required)</span></span>
- <span data-ttu-id="1c73b-524">รัฐ (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-524">State (required)</span></span>
- <span data-ttu-id="1c73b-525">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="1c73b-525">County</span></span> 
- <span data-ttu-id="1c73b-526">เมือง (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="1c73b-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="1c73b-527">ตั้งค่าคอนฟิกข้อมูลของคุณเพื่อสร้างค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="1c73b-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="1c73b-528">ถ้าคุณกำลังสร้างค่าจ้างสำหรับพนักงานในเม็กซิโก ต้องตั้งค่าคอนฟิกองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c73b-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="1c73b-529">ต้องมีแผนกในตำแหน่งต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-529">Departments are required on positions.</span></span>
- <span data-ttu-id="1c73b-530">ศูนย์ต้นทุนต้องถูกตั้งค่าเป็นมิติทางการเงิน และต้องเป็นองค์ประกอบแรกในสตริงมิติทางการเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1c73b-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="1c73b-531">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-531">Job types</span></span>

<span data-ttu-id="1c73b-532">มีการใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="1c73b-533">ชนิดของงานจะต้องใช้เพื่อประมวลผลค่าจ้างในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="1c73b-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="1c73b-534">ตัวอย่างของชนิดงานรวมแบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1c73b-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1c73b-535">ชนิดงานถูกแม็ปไปยัง Dayforce เป็นชนิดค่าจ้างที่บ่งชี้ว่า พนักงานเป็นแบบรายชั่วโมง หรือแบบรับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="1c73b-536">ชนิดงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-537">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-537">Job type</span></span>   | <span data-ttu-id="1c73b-538">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="1c73b-539">ต่อชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1c73b-539">Hourly</span></span>     | <span data-ttu-id="1c73b-540">MX รายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1c73b-540">MX Hourly</span></span>   |
| <span data-ttu-id="1c73b-541">รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-541">Salaried</span></span>   | <span data-ttu-id="1c73b-542">MX รับเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="1c73b-543">ชนิดของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-543">Position types</span></span> 

<span data-ttu-id="1c73b-544">คุณใช้ชนิดของตำแหน่งเพื่ออธิบายว่า ตำแหน่งเป็นแบบเต็มเวลา แบบชั่วคราว หรือแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="1c73b-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="1c73b-545">ชนิดของตำแหน่งถูกแม็ปไปยัง Dayforce เป็นคลาสค่าจ้างที่บ่งชี้ว่าพนักงานเป็นแบบเต็มเวลา หรือแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1c73b-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="1c73b-546">ชนิดของตำแหน่งและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-547">ชนิดของตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="1c73b-547">Position type</span></span>   | <span data-ttu-id="1c73b-548">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="1c73b-549">งานประจำ</span><span class="sxs-lookup"><span data-stu-id="1c73b-549">Full-time</span></span>       | <span data-ttu-id="1c73b-550">พนักงานแบบเต็มเวลา</span><span class="sxs-lookup"><span data-stu-id="1c73b-550">Full time employee</span></span> |
| <span data-ttu-id="1c73b-551">งานชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1c73b-551">Part-time</span></span>       | <span data-ttu-id="1c73b-552">พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1c73b-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="1c73b-553">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="1c73b-553">Reason codes</span></span>

<span data-ttu-id="1c73b-554">รหัสเหตุผลให้ข้อมูลเกี่ยวกับสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="1c73b-555">รหัสเหตุผลถูกแม็ปไปยัง Dayforce เป็นเหตุผลสถานะที่บ่งชี้เหตุผลสำหรับการเปลี่ยนแปลงไปยังสถานะการจ้างงานหรือตำแหน่งงานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="1c73b-556">รหัสเหตุผลและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-557">รหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="1c73b-557">Reason code</span></span>            | <span data-ttu-id="1c73b-558">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-558">Description</span></span>                    | <span data-ttu-id="1c73b-559">สถานการณ์จำลองที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="1c73b-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="1c73b-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="1c73b-561">การออกก่อนค่าจ้างแรก</span><span class="sxs-lookup"><span data-stu-id="1c73b-561">Departure before first payroll</span></span> | <span data-ttu-id="1c73b-562">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-562">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-563">การลาออก</span><span class="sxs-lookup"><span data-stu-id="1c73b-563">RESIGNATION</span></span>            | <span data-ttu-id="1c73b-564">การลาออก</span><span class="sxs-lookup"><span data-stu-id="1c73b-564">Resignation</span></span>                    | <span data-ttu-id="1c73b-565">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-565">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-566">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="1c73b-566">PENSION</span></span>                | <span data-ttu-id="1c73b-567">เงินบำนาญ</span><span class="sxs-lookup"><span data-stu-id="1c73b-567">Pension</span></span>                        | <span data-ttu-id="1c73b-568">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-568">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-569">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-569">TERMINATION</span></span>            | <span data-ttu-id="1c73b-570">การสิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-570">Termination</span></span>                    | <span data-ttu-id="1c73b-571">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-571">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-572">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-572">RETIREMENT</span></span>             | <span data-ttu-id="1c73b-573">การปลดเกษียณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-573">Retirement</span></span>                     | <span data-ttu-id="1c73b-574">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-574">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-575">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-575">ABSENTEE</span></span>               | <span data-ttu-id="1c73b-576">ผู้ขาดงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-576">Absentee</span></span>                       | <span data-ttu-id="1c73b-577">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-577">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-578">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-578">OTHER</span></span>                  | <span data-ttu-id="1c73b-579">เหตุผลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-579">Other Reasons</span></span>                  | <span data-ttu-id="1c73b-580">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-580">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-581">การปิด</span><span class="sxs-lookup"><span data-stu-id="1c73b-581">CLOSURE</span></span>                | <span data-ttu-id="1c73b-582">การปิดของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="1c73b-582">Business Closure</span></span>               | <span data-ttu-id="1c73b-583">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-583">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-584">ความตาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-584">DEATH</span></span>                  | <span data-ttu-id="1c73b-585">เสียชีวิต</span><span class="sxs-lookup"><span data-stu-id="1c73b-585">Death</span></span>                          | <span data-ttu-id="1c73b-586">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-586">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="1c73b-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="1c73b-588">การลาหยุด</span><span class="sxs-lookup"><span data-stu-id="1c73b-588">Leave of Absence</span></span>               | <span data-ttu-id="1c73b-589">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-589">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="1c73b-590">CONTRACTEND</span></span>            | <span data-ttu-id="1c73b-591">จุดสิ้นสุดของสัญญา</span><span class="sxs-lookup"><span data-stu-id="1c73b-591">End of Contract</span></span>                | <span data-ttu-id="1c73b-592">เลิกจ้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-592">Terminate worker</span></span>     |
| <span data-ttu-id="1c73b-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="1c73b-593">SALARYCHANGE</span></span>           | <span data-ttu-id="1c73b-594">การเปลี่ยนแปลงเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="1c73b-594">Change of Salary</span></span>               | <span data-ttu-id="1c73b-595">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="1c73b-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="1c73b-596">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-596">Terms of employment</span></span>

<span data-ttu-id="1c73b-597">มีการใช้เงื่อนไขของการจ้างงาน เพื่อสร้างประเภทและตัวอย่างของการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="1c73b-598">เงื่อนไขถูกแม็ปกับ Dayforce เป็นค่าตัวบ่งชี้การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="1c73b-599">เงื่อนไขการจ้างงานและคำอธิบายต่อไปนี้จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="1c73b-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="1c73b-600">เงื่อนไขการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-600">Terms of employment</span></span>   | <span data-ttu-id="1c73b-601">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="1c73b-602">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="1c73b-602">Regular</span></span>               | <span data-ttu-id="1c73b-603">เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="1c73b-603">Regular</span></span>     |
| <span data-ttu-id="1c73b-604">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="1c73b-604">Direct</span></span>                | <span data-ttu-id="1c73b-605">โดยตรง</span><span class="sxs-lookup"><span data-stu-id="1c73b-605">Direct</span></span>      |
| <span data-ttu-id="1c73b-606">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-606">Internship</span></span>            | <span data-ttu-id="1c73b-607">การฝึกงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-607">Internship</span></span>  |
| <span data-ttu-id="1c73b-608">ถาวร</span><span class="sxs-lookup"><span data-stu-id="1c73b-608">Permanent</span></span>             | <span data-ttu-id="1c73b-609">ถาวร</span><span class="sxs-lookup"><span data-stu-id="1c73b-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="1c73b-610">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="1c73b-610">Marital status</span></span>

<span data-ttu-id="1c73b-611">ค่าสถานภาพการสมรสถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1c73b-612">ตารางต่อไปนี้แสดงวิธีการแม็ปค่าสถานภาพการสมรสไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="1c73b-613">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-613">Talent</span></span>                 | <span data-ttu-id="1c73b-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="1c73b-615">สมรส</span><span class="sxs-lookup"><span data-stu-id="1c73b-615">Married</span></span>                | <span data-ttu-id="1c73b-616">สมรส</span><span class="sxs-lookup"><span data-stu-id="1c73b-616">Married</span></span>                   |
| <span data-ttu-id="1c73b-617">โสด</span><span class="sxs-lookup"><span data-stu-id="1c73b-617">Single</span></span>                 | <span data-ttu-id="1c73b-618">โสด</span><span class="sxs-lookup"><span data-stu-id="1c73b-618">Single</span></span>                    |
| <span data-ttu-id="1c73b-619">หม้าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-619">Widowed</span></span>                | <span data-ttu-id="1c73b-620">หม้าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-620">Widowed</span></span>                   |
| <span data-ttu-id="1c73b-621">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-621">Divorced</span></span>               | <span data-ttu-id="1c73b-622">หย่าร้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-622">Divorced</span></span>                  |
| <span data-ttu-id="1c73b-623">ห้างหุ้นส่วนจดทะเบียน</span><span class="sxs-lookup"><span data-stu-id="1c73b-623">Registered Partnership</span></span> | <span data-ttu-id="1c73b-624">ห้างหุ้นส่วนในประเทศ</span><span class="sxs-lookup"><span data-stu-id="1c73b-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="1c73b-625">None</span><span class="sxs-lookup"><span data-stu-id="1c73b-625">None</span></span>                   | <span data-ttu-id="1c73b-626">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1c73b-627">การอยู่ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-627">Cohabiting</span></span>             | <span data-ttu-id="1c73b-628">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="1c73b-629">เพศ</span><span class="sxs-lookup"><span data-stu-id="1c73b-629">Gender</span></span>

<span data-ttu-id="1c73b-630">การแต่งตั้งเพศถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1c73b-631">ตารางต่อไปนี้แสดงวิธีการแม็ปการแต่งตั้งเพศไปยัง Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="1c73b-632">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-632">Talent</span></span>       | <span data-ttu-id="1c73b-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="1c73b-634">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-634">Male</span></span>         | <span data-ttu-id="1c73b-635">เพศชาย</span><span class="sxs-lookup"><span data-stu-id="1c73b-635">Male</span></span>                      |
| <span data-ttu-id="1c73b-636">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="1c73b-636">Female</span></span>       | <span data-ttu-id="1c73b-637">เพศหญิง</span><span class="sxs-lookup"><span data-stu-id="1c73b-637">Female</span></span>                    |
| <span data-ttu-id="1c73b-638">ไม่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="1c73b-638">Non-specific</span></span> | <span data-ttu-id="1c73b-639">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="1c73b-640">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="1c73b-640">Payment method</span></span>

<span data-ttu-id="1c73b-641">วิธีการชำระเงินให้พนักงานและบริษัทมีวิธีในการอธิบายวิธีการจ่ายเงินแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="1c73b-642">วิธีการชำระเงินถูกแม็ปไปยัง Dayforce และถูกแปล ตามความเหมาะสม ไปยังค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1c73b-643">ตารางต่อไปนี้แสดงวิธีการแม็ปวิธีการชำระเงินกับ Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="1c73b-644">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-644">Talent</span></span>             | <span data-ttu-id="1c73b-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="1c73b-646">เงินสด</span><span class="sxs-lookup"><span data-stu-id="1c73b-646">Cash</span></span>               | <span data-ttu-id="1c73b-647">เงินสด</span><span class="sxs-lookup"><span data-stu-id="1c73b-647">Cash</span></span>                      |
| <span data-ttu-id="1c73b-648">การชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1c73b-648">Electronic Payment</span></span> | <span data-ttu-id="1c73b-649">การโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-649">Transfer</span></span>                  |
| <span data-ttu-id="1c73b-650">ตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="1c73b-650">Check</span></span>              | <span data-ttu-id="1c73b-651">เช็ค</span><span class="sxs-lookup"><span data-stu-id="1c73b-651">Cheque</span></span>                    |
| <span data-ttu-id="1c73b-652">ตั๋วแลกเงินธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1c73b-652">Bank Draft</span></span>         | <span data-ttu-id="1c73b-653">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1c73b-654">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1c73b-654">Other</span></span>              | <span data-ttu-id="1c73b-655">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="1c73b-656">ชนิดของบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="1c73b-656">Bank account type</span></span>

<span data-ttu-id="1c73b-657">ชนิดของบัญชีธนาคารถูกใช้สำหรับการชำระเงินทางอิเล็กทรอนิกส์แก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="1c73b-658">ชนิดบัญชีธนาคารถูกแม็ปกับ Dayforce เป็นข้อมูลบัญชีการโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="1c73b-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="1c73b-659">ชนิดของบัญชีธนาคารจะถูกแปล ตามความเหมาะสม กับค่าที่ยอมรับ เมื่อมีการรวม</span><span class="sxs-lookup"><span data-stu-id="1c73b-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="1c73b-660">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-660">Talent</span></span>            | <span data-ttu-id="1c73b-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="1c73b-662">บัญชีกระแสรายวัน</span><span class="sxs-lookup"><span data-stu-id="1c73b-662">Checking Account</span></span>  | <span data-ttu-id="1c73b-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="1c73b-663">CheckingAccount</span></span>           |
| <span data-ttu-id="1c73b-664">บัญชีเครดิตค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="1c73b-664">Payroll Account</span></span>   | <span data-ttu-id="1c73b-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="1c73b-665">PayrollAccount</span></span>            |
| <span data-ttu-id="1c73b-666">บัญชีออมทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1c73b-666">Savings Account</span></span>   | <span data-ttu-id="1c73b-667">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1c73b-668">บัญชี BankGirot</span><span class="sxs-lookup"><span data-stu-id="1c73b-668">BankGirot account</span></span> | <span data-ttu-id="1c73b-669">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1c73b-670">บัญชี PlusGirot</span><span class="sxs-lookup"><span data-stu-id="1c73b-670">PlusGirot account</span></span> | <span data-ttu-id="1c73b-671">*ไม่รองรับโดยเม็กซิโก*</span><span class="sxs-lookup"><span data-stu-id="1c73b-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="1c73b-672">รหัสรายได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-672">Earning codes</span></span>

<span data-ttu-id="1c73b-673">รหัสรายได้ระบุทุกชนิดของรายได้ทุกชนิดที่ผู้ปฏิบัติงานที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="1c73b-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1c73b-674">รหัสครอบคลุมพารามิเตอร์ต่างๆ ที่เกี่ยวข้องกับรายได้ เช่น กฎทางบัญชี กฎภาษี ข้อกำหนดในการรายงาน และความสามารถในการชำระเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="1c73b-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="1c73b-675">ถ้ามีการใช้ความถี่ที่ไม่สนับสนุน ความถี่ **การชำระค่าจ้างทุกๆ รายการ** จะถูกใช้ตามค่าเริ่มต้นสำหรับการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1c73b-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="1c73b-676">ความถี่ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="1c73b-676">Supported frequencies</span></span>

- <span data-ttu-id="1c73b-677">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1c73b-677">All</span></span>
- <span data-ttu-id="1c73b-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="1c73b-678">EVERYPAY</span></span>
- <span data-ttu-id="1c73b-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="1c73b-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="1c73b-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="1c73b-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="1c73b-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="1c73b-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="1c73b-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-682">1OFMTH</span></span>
- <span data-ttu-id="1c73b-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-683">LASTOFMTH</span></span>
- <span data-ttu-id="1c73b-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-684">2OFMTH</span></span>
- <span data-ttu-id="1c73b-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-685">3OFMTH</span></span>
- <span data-ttu-id="1c73b-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-686">4OFMTH</span></span>
- <span data-ttu-id="1c73b-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-687">5OFMTH</span></span>
- <span data-ttu-id="1c73b-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-688">1N2OFMTH</span></span>
- <span data-ttu-id="1c73b-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-689">3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-690">1N3OFMTH</span></span>
- <span data-ttu-id="1c73b-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-691">1N4OFMTH</span></span>
- <span data-ttu-id="1c73b-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-692">2N3OFMTH</span></span>
- <span data-ttu-id="1c73b-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-693">2N4OFMTH</span></span>
- <span data-ttu-id="1c73b-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="1c73b-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="1c73b-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1c73b-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="1c73b-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="1c73b-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="1c73b-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="1c73b-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="1c73b-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="1c73b-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="1c73b-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="1c73b-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="1c73b-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="1c73b-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="1c73b-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1c73b-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="1c73b-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1c73b-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="1c73b-706">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="1c73b-706">Addresses</span></span>

<span data-ttu-id="1c73b-707">การระบุรหัสประจำตัวของประเทศหรือภูมิภาคเฉพาะ รัฐ และรหัสเขต (เขตปกครอง) ต้องมีรูปแบบเฉพาะที่ Dayforce และผู้ให้บริการในประเทศ/ในเขตสามารถจดจำได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="1c73b-708">แม้ว่ารูปแบบสำหรับเมืองจะยืดหยุ่นได้ เมืองทุกเมืองต้องเชื่อมโยงกับรัฐ</span><span class="sxs-lookup"><span data-stu-id="1c73b-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="1c73b-709">Talent</span><span class="sxs-lookup"><span data-stu-id="1c73b-709">Talent</span></span>              | <span data-ttu-id="1c73b-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="1c73b-711">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="1c73b-711">Country/Region</span></span>      | <span data-ttu-id="1c73b-712">รหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="1c73b-712">Country Code</span></span>          |
| <span data-ttu-id="1c73b-713">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="1c73b-713">Zip/Postal Code</span></span>     | <span data-ttu-id="1c73b-714">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="1c73b-714">Postal Code</span></span>           |
| <span data-ttu-id="1c73b-715">สถานะ</span><span class="sxs-lookup"><span data-stu-id="1c73b-715">State</span></span>               | <span data-ttu-id="1c73b-716">รหัสรัฐ</span><span class="sxs-lookup"><span data-stu-id="1c73b-716">State Code</span></span>            |
| <span data-ttu-id="1c73b-717">เมือง</span><span class="sxs-lookup"><span data-stu-id="1c73b-717">City</span></span>                | <span data-ttu-id="1c73b-718">เมือง</span><span class="sxs-lookup"><span data-stu-id="1c73b-718">City</span></span>                  |
| <span data-ttu-id="1c73b-719">เขตเทศบาล</span><span class="sxs-lookup"><span data-stu-id="1c73b-719">County</span></span>              | <span data-ttu-id="1c73b-720">เขต (เขตปกครอง)</span><span class="sxs-lookup"><span data-stu-id="1c73b-720">County (Municipality)</span></span> |
| <span data-ttu-id="1c73b-721">ถนน</span><span class="sxs-lookup"><span data-stu-id="1c73b-721">Street</span></span>              | <span data-ttu-id="1c73b-722">ที่อยู่ บรรทัดที่ 1</span><span class="sxs-lookup"><span data-stu-id="1c73b-722">Address Line 1</span></span>        |
| <span data-ttu-id="1c73b-723">หมายเลขถนน</span><span class="sxs-lookup"><span data-stu-id="1c73b-723">Street Number</span></span>       | <span data-ttu-id="1c73b-724">ที่อยู่ บรรทัดที่ 2</span><span class="sxs-lookup"><span data-stu-id="1c73b-724">Address Line 2</span></span>        |
| <span data-ttu-id="1c73b-725">ข้อมูลเพิ่มเติมเกี่ยวกับอาคาร</span><span class="sxs-lookup"><span data-stu-id="1c73b-725">Building Complement</span></span> | <span data-ttu-id="1c73b-726">ที่อยู่ บรรทัดที่ 5</span><span class="sxs-lookup"><span data-stu-id="1c73b-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="1c73b-727">หมายเลขหนังสือเดินทาง</span><span class="sxs-lookup"><span data-stu-id="1c73b-727">Passport number</span></span>

<span data-ttu-id="1c73b-728">พนักงานสามารถประกาศข้อมูลหนังสือเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="1c73b-728">Employees can declare passport information.</span></span> <span data-ttu-id="1c73b-729">ข้อมูลนี้เป็นชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง** และถูกรวมอยู่ใน Dayforce เป็นส่วนหนึ่งของข้อมูลเม็กซิโกเฉพาะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1c73b-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="1c73b-730">ชนิดการระบุรหัสประจำตัว = "หนังสือเดินทาง"</span><span class="sxs-lookup"><span data-stu-id="1c73b-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="1c73b-731">วันที่ออก</span><span class="sxs-lookup"><span data-stu-id="1c73b-731">Issued Date</span></span>
- <span data-ttu-id="1c73b-732">วันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="1c73b-732">Expiration Date</span></span>

<span data-ttu-id="1c73b-733">พนักงานสามารถประกาศหมายเลขรหัสหลายเลขของชนิดการระบุรหัสประจำตัว **หนังสือเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="1c73b-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="1c73b-734">อย่างไรก็ตาม เฉพาะรายการหนังสือเดินทางที่ใช้งานปัจจุบันจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="1c73b-735">ถ้ารายการหนังสือเดินทางทั้งหมดหมดอายุ หนังสือเดินทางที่ออกครั้งล่าสุดจะถูกรวมอยู่ใน Dayforce</span><span class="sxs-lookup"><span data-stu-id="1c73b-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
