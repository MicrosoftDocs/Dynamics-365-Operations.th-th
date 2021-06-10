---
title: สร้างรายงานกฎหมายประกันสุขภาพ (Affordable Care Act (ACA))
description: การรายงานของ Affordable Care Act (ACA) สร้างแบบฟอร์ม 1095-B และ 1095-C เพื่อสนับสนุนส่วน **ข้อบังคับนายจ้าง** ของ Affordable Care Act
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053212"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="1fcf7-103">สร้างรายงาน ACA</span><span class="sxs-lookup"><span data-stu-id="1fcf7-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1fcf7-104">การรายงานของ Affordable Care Act (ACA) สร้างแบบฟอร์ม 1095-B และ 1095-C เพื่อสนับสนุนส่วน **ข้อบังคับนายจ้าง** ของ Affordable Care Act</span><span class="sxs-lookup"><span data-stu-id="1fcf7-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="1fcf7-105">การรายงาน ACA เปิดใช้งานเฉพาะกับนิติบุคคลในสหรัฐอเมริกาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1fcf7-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="1fcf7-106">การเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1fcf7-106">Getting started</span></span>

<span data-ttu-id="1fcf7-107">เมื่อต้องการติดตามข้อมูลฟอร์ม 1095-B และ 1095-C ก่อนอื่น คุณต้องสร้างกลุ่มความคุ้มครอง Affordable Care หนึ่งกลุ่มหรือมากกว่านั้น</span><span class="sxs-lookup"><span data-stu-id="1fcf7-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="1fcf7-108">กลุ่มความคุ้มครอง Affordable Care ระบุ:</span><span class="sxs-lookup"><span data-stu-id="1fcf7-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="1fcf7-109">ข้อเสนอความคุ้มครองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="1fcf7-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="1fcf7-110">ส่วนแบ่งของพนักงานของค่าจ้างพิเศษรายเดือนที่มีต้นทุนต่ำสุด ถ้าต้นทุนสูงกว่าบรรทัดความยากจนของรัฐบาลกลาง</span><span class="sxs-lookup"><span data-stu-id="1fcf7-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="1fcf7-111">การรักษาข้อมูลส่วนบุคคลที่ใช้โดยนายจ้าง ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="1fcf7-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="1fcf7-112">กลุ่มความคุ้มครอง Affordable Care ช่วยให้คุณสามารถจัดการข้อมูลสำหรับฟิลด์เหล่านี้ได้ โดยไม่ต้องเปลี่ยนแปลงเรกคอร์ดของพนักงานทุกคนที่มีเงื่อนไขเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="1fcf7-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="1fcf7-113">คุณยังสามารถมอบหมายกลุ่มความคุ้มครอง Affordable Care ให้กับพนักงานอย่างน้อยหนึ่งคนได้อย่างง่ายดาย โดยใช้ฟังก์ชัน **การกำหนดจำนวนมาก** ในหน้า</span><span class="sxs-lookup"><span data-stu-id="1fcf7-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="1fcf7-114">การรักษากลุ่มความคุ้มครองหลายเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="1fcf7-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="1fcf7-115">คุณสามารถรักษากลุ่มความคุ้มครองหลายรุ่น</span><span class="sxs-lookup"><span data-stu-id="1fcf7-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="1fcf7-116">ฟังก์ชันนี้ช่วยให้คุณสามารถเปลี่ยนแปลงได้โดยไม่สร้างกลุ่มใหม่และกำหนดพนักงานใหม่ให้กับกลุ่มใหม่</span><span class="sxs-lookup"><span data-stu-id="1fcf7-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="1fcf7-117">หลังจากที่คุณสร้างกลุ่มความคุ้มครอง ACA แล้ว คุณสามารถกําหนดกลุ่มโดยรวมให้กับพนักงานด้วยตัวเลือก **การกำหนดจำนวนมาก** ได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="1fcf7-118">นอกจากนี้คุณยังสามารถระบุได้ว่าจะติดตามและรายงานข้อมูล ACA หรือไม่ และกําหนดพนักงานให้กับลุ่มความคุ้มครองชุดนั้น</span><span class="sxs-lookup"><span data-stu-id="1fcf7-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="1fcf7-119">คุณไม่ต้องติดตามข้อมูลความคุ้มครองของ ACA เช่น พนักงานแบบชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="1fcf7-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="1fcf7-120">ในกรณีนี้ จะมีการตั้งค่าในฟิลด์ **รายงานความคุ้มครอง** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="1fcf7-121">แม้ว่าคุณจะต้องกําหนดพนักงานแต่ละคนที่มีข้อมูล ACA ที่สามารถติดตามได้ให้กับกลุ่มความคุ้มครอง Affordable Care แต่คุณยังสามารถเปลี่ยนตัวเลือกต่อไปนี้เป็นเดือนโดยมีค่าที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="1fcf7-122">**ข้อเสนอความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-122">**Offer of coverage**</span></span>
- <span data-ttu-id="1fcf7-123">**ค่าจ่ายร่วมของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-123">**Employee share of cost**</span></span>
- <span data-ttu-id="1fcf7-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-124">**Safe Harbor**</span></span>

<span data-ttu-id="1fcf7-125">เมื่อต้องการป้อนข้อยกเว้นในค่าใด ๆ ของกลุ่มความคุ้มครอง Affordable Care เลือกที่ลิงค์ **ความคุ้มครอง Affordable Care** ที่พบในหน้า **รายละเอียดผู้ปฏิบัติงาน** ซึ่งอยู่ใต้ส่วน **ข้อมูลเพิ่มเติม** บน **แท็บการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="1fcf7-126">การรายงานความคุ้มครองสุขภาพ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-126">Reporting health care coverage</span></span>

<span data-ttu-id="1fcf7-127">นอกเหนือจากการติดตาม สมมติว่ามีการนำเสนอความคุ้มครองการประกันสุขภาพประกันใด ๆ ให้แก่พนักงานเต็มเวลา ถ้าความคุ้มครองสุขภาพแบบประกันด้วยตนเองที่สนับสนุนโดยนายจ้าง ซึ่งพนักงานได้มีการลงทะเบียนให้ (โดยไม่คำนึงว่าสถานะของการจ้างงานเป็นแบบชั่วคราวหรือเต็มเวลา) ข้อมูลเพิ่มเติมจำเป็นต้องถูกรายงานใน 1095-C</span><span class="sxs-lookup"><span data-stu-id="1fcf7-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="1fcf7-128">พนักงานแต่ละคน (รวมทั้งผู้อยู่ในอุปการะ) ที่ได้รับการคุ้มครองโดยแผนสวัสดิการที่สนับสนุนโดยนายจ้าง ต้องถูกรวมไว้ในรายงานสำหรับเดือนพวกเขาได้รับการคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="1fcf7-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="1fcf7-129">คุณสามารถระบุว่าต้องมีการรายงานแผนสวัสดิการแต่ละรายการหรือไม่ โดยเลือกกล่องกาเครื่องหมาย **ต้องรายงาน ACA**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="1fcf7-130">นอกจากนี้ ถ้าพนักงานได้เลือกที่จะให้ผู้อยู่ในอุปการะได้รับความคุ้มครองภายใต้สวัสดิการ คุณสามารถระบุวันที่ที่ผู้อยู่ในอุปการะได้รับการคุ้มครองสำหรับพนักงานแต่ละคนในหน้า **รักษาสวัสดิการ**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="1fcf7-131">เมื่อต้องการบ่งชี้ว่า มีการคุ้มครองผู้อยู่ในอุปการะภายใต้สวัสดิการ เลือกปุ่ม **แก้ไข** ในบานหน้าต่างการดำเนินการของแท็บด่วน **ผู้อยู่ในอุปการะ**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="1fcf7-132">ในหน้า **ตัวจัดการวันที่คุ้มครองผู้อยู่ในอุปการะ** คุณสามารถระบุวันที่ที่ผู้อยู่ในอุปการะได้รับการคุ้มครองโดยสวัสดิการได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="1fcf7-133">การป้อนวันที่ในหน้านี้จะเลือกกล่องกาเครื่องหมาย **ได้รับการคุ้มครอง** ในหน้า **รักษาสวัสดิการ** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="1fcf7-134">สร้างแบบฟอร์ม 1095-B และ 1095-C</span><span class="sxs-lookup"><span data-stu-id="1fcf7-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="1fcf7-135">คุณยังสามารถสร้างแบบฟอร์ม 1095-B และ 1095-C จากภายในผลิตภัณฑ์ และกระจายให้กับพนักงานของคุณแต่ละคนได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="1fcf7-136">ระบบยังสามารถสร้างฟอร์ม 1095-C และไฟล์การส่งสินค้า 1094-C IRS ทางอิเล็กทรอนิกส์ได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="1fcf7-137">เมื่อสร้างแบบฟอร์ม 1095-C ป้อนในปีภาษีที่เหมาะสม และบ่งชี้ว่าควรมาสก์หมายเลขประกันสังคมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1fcf7-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="1fcf7-138">ถ้าคุณกำลังพิมพ์ฟอร์ม 1095-C สำหรับพนักงานมากกว่า 500 ราย คุณจะได้รับไฟล์ PDF มากกว่าหนึ่งไฟล์</span><span class="sxs-lookup"><span data-stu-id="1fcf7-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="1fcf7-139">ขอแนะนำให้คุณเพิ่ม **ขนาดไฟล์สูงสุด** ในหน้าต่าง **พารามิเตอร์การจัดการเอกสาร** สูงสุดถึง 150 MB</span><span class="sxs-lookup"><span data-stu-id="1fcf7-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="1fcf7-140">การดูข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1fcf7-140">Viewing information</span></span>

<span data-ttu-id="1fcf7-141">คุณสามารถใช้หน้า **ความคุ้มครอง Affordable Care ของผู้ปฏิบัติงาน** เพื่อดูว่าพนักงานคนใดถูกกำหนดให้กับกลุ่มความคุ้มครองแต่ละกลุ่ม พนักงานคนใดไม่จำเป็นต้องถูกรวมอยู่ในรายงาน และพนักงานคนใดที่ยังไม่ได้ถูกกำหนด</span><span class="sxs-lookup"><span data-stu-id="1fcf7-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="1fcf7-142">ถ้ามีการแทนที่ค่าเริ่มต้นใด ๆ จากกลุ่มความคุ้มครอง Affordable Care เครื่องหมายดอกจันจะปรากฏขึ้นถัดจากค่าที่ถูกเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="1fcf7-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="1fcf7-143">ถ้าค่าสำหรับทั้งหมด 12 เดือนเหมือนกัน และไม่ได้ถูกแทนที่ มูลค่าจะพิมพ์ในคอลัมน์ **ทั้งหมด 12 เดือน**</span><span class="sxs-lookup"><span data-stu-id="1fcf7-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="1fcf7-144">คุณยังสามารถใช้หน้าต่างการสอบถามเพื่อความเข้าใจว่าพนักงานคนใดได้รับแฟล็กเป็นไม่รายงาน ACA</span><span class="sxs-lookup"><span data-stu-id="1fcf7-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="1fcf7-145">คุณไม่จำเป็นต้องติดตามว่ามีการเสนอความคุ้มครองหรือไม่ และไม่จำเป็นต้องออก 1095-C เมื่อสิ้นสุดปี</span><span class="sxs-lookup"><span data-stu-id="1fcf7-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="1fcf7-146">เลือก **ไม่รายงาน ACA** ในฟิลด์ **กรองตาม** เพื่อสร้างรายชื่อของพนักงานทั้งหมดที่จะไม่ได้รับ 1095-C</span><span class="sxs-lookup"><span data-stu-id="1fcf7-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="1fcf7-147">นอกจากนี้ คุณยังสามารถดูพนักงานใด ๆ ที่ยังถูกไม่ได้กำหนด (ฟิลด์ **ความคุ้มครองรายงาน ACA** จะว่างเปล่า) หรือถูกกำหนดให้กับกลุ่มความคุ้มครอง Affordable Care ที่หมดอายุสำหรับปีที่เลือกในฟิลด์ **ปี** ได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="1fcf7-148">คุณสามารถส่งออกรายชื่อของพนักงานที่ถูกสร้างขึ้นโดยใช้ตัวเลือกการกรองไปยัง Excel ได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="1fcf7-149">หากคุณต้องรายงานผู้อยู่ในอุปการะที่ครอบคลุม เนื่องจากคุณให้ความคุ้มครองในการประกันภัยตนเอง คุณสามารถดูผู้อยู่ในอุปการะที่ครอบคลุมภายใต้แผนสวัสดิการ ที่มีการทำเครื่องหมายเป็น **ACA ที่สามารถรายงาน** ได้</span><span class="sxs-lookup"><span data-stu-id="1fcf7-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="1fcf7-150">เลือก **ดูการคุ้มครองผู้อยู่ในอุปการะ** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1fcf7-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="1fcf7-151">เฉพาะแผนสวัสดิการที่ทำเครื่องหมายเป็นการแสดงผล **ACA สามารถรายงาน** ในหน้าต่างการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1fcf7-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]