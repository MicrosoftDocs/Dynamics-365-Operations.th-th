---
title: ตั้งค่าคอนฟิกพารามิเตอร์ Human Resources
description: หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ทรัพยากรบุคคลเฉพาะบริษัท ใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052420"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="95668-103">ตั้งค่าคอนฟิกพารามิเตอร์ Human Resources</span><span class="sxs-lookup"><span data-stu-id="95668-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="95668-104">การตั้งค่าพารามิเตอร์ทรัพยากรบุคคลบางรายการมีการใช้ร่วมกันระหว่างบริษัท ในขณะที่การตั้งค่าของพารามิเตอร์อื่นๆ ใช้เฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="95668-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="95668-105">หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ทรัพยากรบุคคลเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="95668-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="95668-106">สองหน้าจะถูกใช้เพื่อตั้งค่าพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="95668-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="95668-107">สำหรับพารามิเตอร์ที่ถูกใช้ร่วมกันระหว่างบริษัท คุณใช้หน้า **พารามิเตอร์ที่ใช้ร่วมกันของฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="95668-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="95668-108">สำหรับพารามิเตอร์ที่เฉพาะบริษัท (กล่าวคือ การตั้งค่าจะนำไปใช้กับบริษัทเดียว) คุณใช้หน้า **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="95668-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![ไปที่พารามิเตอร์ทรัพยากรบุคคล](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="95668-110">ในหน้า **พารามิเตอร์ทรัพยากรบุคคล** การตั้งค่าถูกแบ่งเป็นหกแท็บ:</span><span class="sxs-lookup"><span data-stu-id="95668-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="95668-111">**ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="95668-111">**General**</span></span>
- <span data-ttu-id="95668-112">**การสรรหาบุคลากร** (แท็บนี้ไม่ถูกรวมอยู่ใน Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="95668-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="95668-113">**ค่าตอบแทน**</span><span class="sxs-lookup"><span data-stu-id="95668-113">**Compensation**</span></span>
- <span data-ttu-id="95668-114">**ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="95668-114">**Number sequences**</span></span>
- <span data-ttu-id="95668-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="95668-115">**FMLA**</span></span>
- <span data-ttu-id="95668-116">**ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="95668-116">**Employee self service**</span></span>
- <span data-ttu-id="95668-117">**ระบบบริการตนเองของผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="95668-117">**Manager self service**</span></span>
- <span data-ttu-id="95668-118">**การจัดการสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="95668-118">**Benefits management**</span></span>
- <span data-ttu-id="95668-119">**การลางานและการขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="95668-119">**Leave and absence**</span></span>
- <span data-ttu-id="95668-120">**วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="95668-120">**Payment methods**</span></span>

<span data-ttu-id="95668-121">แต่ละแท็บประกอบด้วยข้อมูลที่เกี่ยวข้องกับบริษัทเดียว</span><span class="sxs-lookup"><span data-stu-id="95668-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="95668-122">ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="95668-122">General</span></span>

<span data-ttu-id="95668-123">การตั้งค่าบนแท็บ **ทั่วไป** กำหนดรูปลักษณ์ของข้อมูลเกี่ยวกับการขาดงาน การบาดเจ็บและการเจ็บป่วย และการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="95668-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="95668-124">การตั้งค่าบนแท็บนี้ยังกำหนดบางรายการเริ่มต้นที่ปรากฏขึ้นเมื่อคุณทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="95668-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="95668-125">กล่าวคือ แท็บนี้จะช่วยให้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="95668-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="95668-126">เลือกสีที่จะใช้กับธุรกรรมการขาดงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="95668-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="95668-127">ระบุรูปแบบของแผ่นงานที่จะใช้สำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="95668-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="95668-128">เปิดใช้งานการรวมระหว่างหลักสูตรการฝึกอบรม และการลงทะเบียนการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="95668-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="95668-129">เลือกรหัสการขาดงานที่ใช้ในการควบคุมการรวมนี้</span><span class="sxs-lookup"><span data-stu-id="95668-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="95668-130">บ่งชี้ว่าจะเก็บเหตุการณ์กรณีการบาดเจ็บและการเจ็บป่วยไว้นานเท่าใด</span><span class="sxs-lookup"><span data-stu-id="95668-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="95668-131">ระบุหมายเลขรหัสประจำตัวเริ่มต้นที่แสดงเมื่อมีจ้างงานผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="95668-131">Specify the default identification number shown when a new worker is hired.</span></span>

![แท็บทั่วไป](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="95668-133">การสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="95668-133">Recruitment</span></span>

<span data-ttu-id="95668-134">การตั้งค่าบนแท็บ **การสรรหาบุคลากร** จะกําหนดชนิดเอกสารที่ใช้สำหรับจดหมายโต้ตอบที่ส่งให้กับผู้สมัครโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="95668-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="95668-135">คุณยังสามารถระบุโครงการสรรหาบุคลากรที่ใช้กับใบสมัครที่ไม่ได้ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="95668-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="95668-136">รอบระยะเวลาที่ถูกกำหนดไว้สำหรับโครงการสรรหาบุคลากรที่กำหนดอายุ โครงการสรรหาบุคลากรที่จะรวมอยู่ในไทล์ **อายุหนี้โครงการ** ในพื้นที่ทำงาน **จัดการสรรหาบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="95668-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="95668-137">รอบระยะเวลาที่ถูกกำหนดไว้สำหรับคำเตือนเวลาสิ้นสุดของใบสมัคร จะถูกใช้เพื่อแสดงโครงการสรรหาบุคลากรที่จะใกล้ครบกำหนดเวลาสิ้นสุดของใบสมัครในไทล์ **การใกล้วันครบกำหนดเวลาสิ้นสุดของใบสมัคร** ในพื้นที่ทำงาน **การสรรหาบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="95668-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="95668-138">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสรรหาบุคลากร ให้ดูที่ [สรรหาผู้สมัครงาน](hr-personnel-recruit.md)</span><span class="sxs-lookup"><span data-stu-id="95668-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="95668-139">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="95668-139">Compensation</span></span>

<span data-ttu-id="95668-140">ใน Dynamics 365 Finance การตั้งค่าบนแท็บ **ค่าตอบแทน** กำหนดว่าผู้ใช้ต้องยืนยันว่า พวกเขาต้องการบันทึกข้อมูลสำหรับแผนค่าตอบแทนคงที่ หรือผันแปร</span><span class="sxs-lookup"><span data-stu-id="95668-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="95668-141">หากคุณเลือก **เปิดใช้งานบันทึกการตรวจสอบความถูกต้อง** เมื่อผู้ใช้ปิดหน้าค่าตอบแทนที่เกี่ยวข้อง พวกเขาจะได้รับข้อความที่ถามว่า พวกเขาต้องการบันทึกเรกคอร์ดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="95668-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="95668-142">บางหน้าในการจัดการค่าตอบแทน ไม่อนุญาตให้ผู้ใช้ลบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="95668-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="95668-143">โดยกระตุ้นผู้ใช้ให้ตรวจสอบว่าพวกเขาต้องการบันทึกข้อมูล คุณอาจสามารถจำกัดจำนวนของข้อมูลที่ถูกบันทึกไว้ แต่ไม่สามารถลบได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="95668-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="95668-144">หากคุณล้าง **เปิดใช้งานบันทึกการตรวจสอบความถูกต้อง** เรกคอร์ดจะถูกบันทึกทันที อาจก่อนที่ผู้ใช้พร้อม</span><span class="sxs-lookup"><span data-stu-id="95668-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="95668-145">ถ้าคุณกำลังใช้การจัดการประสิทธิภาพ แท็บ **ค่าตอบแทน** ยังช่วยให้คุณเลือกแบบจำลองที่จัดอันดับเพื่อใช้แทนแบบจำลองที่กำหนดให้กับแผนค่าตอบแทน เมื่อมีการจัดอันดับประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="95668-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="95668-146">ในทรัพยากรบุคคล คุณสามารถใช้แท็บ **ค่าตอบแทน** เพื่อเลือกเพื่อจํากัดการเข้าถึงแผนค่าตอบแทน และตั้งค่าสกุลเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="95668-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="95668-147">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับค่าตอบแทน โปรดดู [ภาพรวมของแผนค่าตอบแทน](hr-compensation-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95668-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![แท็บค่าตอบแทน](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="95668-149">ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="95668-149">Number sequences</span></span>

<span data-ttu-id="95668-150">การตั้งค่าบนแท็บ **ลำดับหมายเลข** จะกําหนดลำดับที่ใช้ในการกําหนดรหัสให้กับรายการในทรัพยากรบุคคลโดยอัตโนมัติ เช่น:</span><span class="sxs-lookup"><span data-stu-id="95668-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="95668-151">การสมัคร</span><span class="sxs-lookup"><span data-stu-id="95668-151">Applications</span></span>
- <span data-ttu-id="95668-152">การลงทะเบียนการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="95668-152">Absence registrations</span></span>
- <span data-ttu-id="95668-153">ผลลัพธ์ของกระบวนการค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="95668-153">Compensation process results</span></span>
- <span data-ttu-id="95668-154">หมายเลขกรณี</span><span class="sxs-lookup"><span data-stu-id="95668-154">Case numbers</span></span>
- <span data-ttu-id="95668-155">หลักสูตร</span><span class="sxs-lookup"><span data-stu-id="95668-155">Courses</span></span>
- <span data-ttu-id="95668-156">วาระการประชุมของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="95668-156">Course agendas</span></span>

<span data-ttu-id="95668-157">การรักษาการอ้างอิงลำดับหมายเลขและรหัส ใช้หน้ารายการ **ลำดับหมายเลข** (เลือก **การจัดการองค์กร > ลำดับหมายเลข > ลำดับหมายเลข**)</span><span class="sxs-lookup"><span data-stu-id="95668-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="95668-158">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของลำดับหมายเลข](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="95668-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="95668-159">จำนวนชั่วโมงที่ทำงานต้องไม่เกินจำนวน 1250 ชั่วโมงและความยาวของการจ้างงานต้องไม่เกิน 12 เดือน</span><span class="sxs-lookup"><span data-stu-id="95668-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="95668-160">ค่าสูงสุดเหล่านี้จะสอดคล้องกับกฎหมายในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="95668-160">These maximum values are in accordance with federal law in the United States.</span></span>

![แท็บลำดับหมายเลข](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="95668-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="95668-162">FMLA</span></span>

<span data-ttu-id="95668-163">บนแท็บ FMLA ให้คุณตั้งค่าข้อกำหนดการมีสิทธิ์ FMLA และชั่วโมงการมีสิทธิ์ FMLA</span><span class="sxs-lookup"><span data-stu-id="95668-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="95668-164">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน](hr-leave-and-absence-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="95668-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![แท็บ FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="95668-166">ระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="95668-166">Employee self service</span></span>

<span data-ttu-id="95668-167">การตั้งค่าบนแท็บ **ระบบบริการตนเองของพนักงาน** จะมีผลต่อการที่ระบบบริการตนเองของพนักงานปรากฏต่อพนักงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="95668-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="95668-168">บนแท็บนี้ คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="95668-168">On this tab, you can:</span></span>

- <span data-ttu-id="95668-169">ป้อนชื่อพื้นที่ทำงานระบบบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="95668-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="95668-170">เลือกข้อมูลที่ผู้จัดการสามารถป้อนให้กับพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="95668-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="95668-171">เพิ่มลิงค์ที่เป็นประโยชน์ให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="95668-171">Add useful links for employees</span></span>
- <span data-ttu-id="95668-172">จํากัดพนักงานจากการเพิ่มหรือแก้ไขรายละเอียดผู้ติดต่อทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="95668-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="95668-173">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จำกัดการแก้ไขข้อมูลส่วนบุคคล](hr-employee-self-service-restrict-editing.md)</span><span class="sxs-lookup"><span data-stu-id="95668-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="95668-174">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าระบบบริการตนเองของพนักงาน ให้ดูที่ [ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ](hr-employee-manager-self-service-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95668-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![แท็บระบบบริการตนเองของพนักงาน](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="95668-176">ระบบบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="95668-176">Manager self service</span></span>

<span data-ttu-id="95668-177">การตั้งค่าบนแท็บ **ระบบบริการตนเองของผู้จัดการ** จะส่งผลต่อสิ่งที่ผู้จัดการจะเห็นในระบบบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="95668-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="95668-178">บนแท็บนี้ คุณสามารถตั้งค่าตัวเลือกร์ต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="95668-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="95668-179">ช่วงของเรกคอร์ดที่หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="95668-179">The range for expiring records</span></span>
- <span data-ttu-id="95668-180">ผู้จัดการข้อมูลสามารถดูในเรกคอร์ดที่หมดอายุได้</span><span class="sxs-lookup"><span data-stu-id="95668-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="95668-181">ผู้จัดการสามารถดูตําแหน่งที่เปิดของรายงานแบบขยายได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="95668-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="95668-182">มุมมองของผู้ปฏิบัติงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="95668-182">Views of exiting workers</span></span>
- <span data-ttu-id="95668-183">ลิงค์ที่เป็นประโยชน์สำหรับผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="95668-183">Useful links for managers</span></span>

<span data-ttu-id="95668-184">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าระบบบริการตนเองของผู้จัดการ ให้ดูที่ [ภาพรวมของระบบบริการตนเองของพนักงานและผู้จัดการ](hr-employee-manager-self-service-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95668-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![แท็บระบบบริการตนเองของผู้จัดการ](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="95668-186">การจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="95668-186">Benefits management</span></span>

<span data-ttu-id="95668-187">บนแท็บ การจัดการสวัสดิการ คุณสามารถตั้งค่าคอนฟิกตัวเลือกอีเมลเพื่อการจัดการสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="95668-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="95668-188">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าและการใช้การจัดการสวัสดิการ โปรดดู [ภาพรวมของการจัดการสวัสดิการ](hr-benefits-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95668-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![แท็บการจัดการสวัสดิการ](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="95668-190">การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="95668-190">Leave and absence</span></span>

<span data-ttu-id="95668-191">สำหรับข้อมูลเกี่ยวกับการตั้งค่าและการใช้การลางานและการหยุดงาน โปรดดู [ภาพรวมการลางานและการขาดงาน](hr-leave-and-absence-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95668-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="95668-192">วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="95668-192">Payment methods</span></span>

<span data-ttu-id="95668-193">บนแท็บ **วิธีการจ่ายเงิน** คุณสามารถเลือกวิธีการเงินที่องค์กรของคุณสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="95668-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="95668-194">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าคอนฟิกค่าตอบแทน โปรดดู [ภาพรวมของแผนค่าตอบแทน](hr-compensation-overview.md)</span><span class="sxs-lookup"><span data-stu-id="95668-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![แท็บวิธีการจ่ายเงิน](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]