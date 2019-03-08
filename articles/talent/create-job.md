---
title: ตั้งค่าส่วนประกอบของงาน
description: หัวข้อนี้อธิบายถึงองค์ประกอบแนวคิดสามารถรวมงาน และแสดงตัวอย่างของวิธีการที่คุณสามารถใช้องค์ประกอบเหล่านั้นในองค์กรของคุณ
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48787d1eb662322c726698573b27023ae9eed56f
ms.sourcegitcommit: 68df883200b5c477ea1799cc28d3ef467cd29202
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/07/2019
ms.locfileid: "377170"
---
# <a name="set-up-the-components-of-a-job"></a><span data-ttu-id="c011c-103">ตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-103">Set up the components of a job</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="c011c-104">หัวข้อนี้อธิบายถึงองค์ประกอบแนวคิดสามารถรวมงาน และแสดงตัวอย่างของวิธีการที่คุณสามารถใช้องค์ประกอบเหล่านั้นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c011c-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="c011c-105">ก่อนที่คุณจะสามารถสร้างงาน คุณต้องตั้งค่าข้อมูลอ้างอิงบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="c011c-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="c011c-106">คุณสามารถสร้างงานที่มีชื่อเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c011c-106">You can create a job that has only a name.</span></span> <span data-ttu-id="c011c-107">อย่างไรก็ตาม คุณสามารถระบุค่าเริ่มต้นสำหรับตำแหน่งที่กำหนดให้แก่งานได้โดยการรวมข้อมูลเพิ่มเติม เช่น ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="c011c-108">นอกจากนี้ยังสามารถใช้ข้อมูลบางอย่างที่คุณป้อนในการกรองข้อมูลแผนค่าตอบแทนสำหรับงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c011c-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="c011c-109">ถ้าคุณต้องการตั้งค่าสิทธิ์ที่คุณสามารถใช้เพื่อกรองข้อมูลแผนค่าตอบแทนกับงานที่ระบุ คุณควรตั้งค่าฟังก์ชันงานและชนิดงานก่อนที่คุณจะตั้งค่างาน</span><span class="sxs-lookup"><span data-stu-id="c011c-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="c011c-110">คุณจะประหยัดเวลาเมื่อคุณเพิ่มตำแหน่งงานได้เมื่อมีค่าเริ่มต้นเหล่านี้ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c011c-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="c011c-111">รายละเอียดงานบางอย่าง เช่น ตำแหน่งงาน ชนิดงาน และฟังก์ชันงาน คือวันที่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="c011c-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="c011c-112">ถ้าคุณสร้างงานวันนี้ แต่ไม่ได้เพิ่มรายละเอียดเหล่านี้โดยทันที เมื่อคุณดูงาน ณ วันที่สร้าง รายละเอียดเหล่านี้จะไม่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c011c-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="c011c-113">ดังนั้น คุณควรสร้างข้อมูลอ้างอิงนี้บางส่วนก่อนที่คุณจะต้องใช้</span><span class="sxs-lookup"><span data-stu-id="c011c-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="c011c-114">วิธีนี้ คุณสามารถเพิ่มข้อมูลไปยังงานใหม่ได้ขณะที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="c011c-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="c011c-115">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-115">Job titles</span></span>
<span data-ttu-id="c011c-116">ก่อนที่คุณจะสร้างงาน คุณต้องตั้งชื่อสำหรับงานเหล่านั้น </span><span class="sxs-lookup"><span data-stu-id="c011c-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="c011c-117">โดยตำแหน่งจะสืบทอดตำแหน่งงานจากงานที่เชื่อมโยงกับตำแหน่งนั้น</span><span class="sxs-lookup"><span data-stu-id="c011c-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="c011c-118">รักษาตำแหน่งงานได้ที่หน้า **ตำแหน่ง** ซึ่งคุณสามารถเปิดได้โดยใช้ฟังก์ชันการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c011c-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="c011c-119">บนหน้า **ตำแหน่ง** ป้อนตำแหน่งที่คุณวางแผนที่จะใช้สำหรับงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c011c-119">On the \*\*Titles \*\*page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="c011c-120">ชนิดงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-120">Job types</span></span>
<span data-ttu-id="c011c-121">คุณใช้ชนิดงานเพื่อจัดกลุ่มงานที่คล้ายกันเป็นประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c011c-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="c011c-122">ไม่จำเป็นต้องใช้ชนิดงาน </span><span class="sxs-lookup"><span data-stu-id="c011c-122">Job types aren't required.</span></span> <span data-ttu-id="c011c-123">อย่างไรก็ตาม ถ้าคุณวางแผนที่จะใช้ชนิดงานเมื่อคุณตั้งค่ากฎการมีสิทธิ์สำหรับการจัดการค่าตอบแทน คุณควรตั้งค่าชนิดงานก่อนที่คุณตั้งค่างาน </span><span class="sxs-lookup"><span data-stu-id="c011c-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="c011c-124">ตัวอย่างของชนิดงาน เช่น แบบเต็มเวลาและแบบชั่วคราว หรือแบบชำระค่าจ้างรายเดือนและรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c011c-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c011c-125">คุณสามารถรักษาชนิดของงานได้ที่หน้า **ชนิดของงาน**</span><span class="sxs-lookup"><span data-stu-id="c011c-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="c011c-126">บนหน้า **ชนิดของงาน** ป้อนชื่อและคำอธิบายโดยย่อของชนิดของงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="c011c-127">ในฟิลด์ **สถานะยกเว้น** เลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้เพื่อบ่งชี้สถานะยกเว้นของ ฎหมายมาตรฐานแรงงานที่เป็นธรรม (FLSA) ของงานที่มีงานชนิดนี้:</span><span class="sxs-lookup"><span data-stu-id="c011c-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="c011c-128">**ยกเว้น** – งานที่ไม่ได้ยกเว้นจากงานล่วงเวลาภายใต้ FLSA</span><span class="sxs-lookup"><span data-stu-id="c011c-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="c011c-129">**ไม่ได้รับยกเว้น** – งานที่ไม่ได้ยกเว้นจากงานล่วงเวลาภายใต้ FLSA</span><span class="sxs-lookup"><span data-stu-id="c011c-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="c011c-130">**ไม่สามารถใช้** – ไม่สามารถใช้ความครอบคลุมของ FLSA ได้</span><span class="sxs-lookup"><span data-stu-id="c011c-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="c011c-131">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-131">Job functions</span></span>
<span data-ttu-id="c011c-132">ฟังก์ชันงานอธิบายถึงประเภทฟังก์ชันระดับสูงและหน้าที่ระดับสูงที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c011c-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="c011c-133">ไม่จำเป็นต้องใช้ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-133">Job functions aren't required.</span></span> <span data-ttu-id="c011c-134">คุณสามารถใช้ฟังก์ชันงานร่วมกับชนิดงาน เพื่อกรองข้อมูลแผนค่าตอบแทนสำหรับงานที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="c011c-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="c011c-135">คุณสามารถเชื่อมโยงฟังก์ชันงานและชนิดงานกับแผนค่าตอบแทนได้ ด้วยการตั้งค่ากฎการมีคุณสมบัติเหมาะสมในหน้า **กฎการมีคุณสมบัติเหมาะสม**</span><span class="sxs-lookup"><span data-stu-id="c011c-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="c011c-136">คุณยังสามารถแนบชุดของระดับกับแผนค่าตอบแทนที่จะใช้กับชุดชนิดงาน/ฟังก์ชันงานเฉพาะ ซึ่งคุณกำหนดไว้โดยผ่านกฎการมีคุณสมบัติเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c011c-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="c011c-137">(ลักษณะการทำงานเหล่านี้จะใช้กับทั้งแผนค่าตอบแทนคงที่และผันแปร) อย่างไรก็ตาม ถ้าคุณวางแผนที่จะใช้ฟังก์ชันงานเมื่อคุณตั้งค่ากฎการมีสิทธิ์สำหรับการจัดการค่าตอบแทน คุณควรตั้งค่าฟังก์ชันงานก่อนที่คุณตั้งค่างาน</span><span class="sxs-lookup"><span data-stu-id="c011c-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="c011c-138">ตารางต่อไปนี้แสดงตัวอย่างของฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="c011c-139">งาน</span><span class="sxs-lookup"><span data-stu-id="c011c-139">Job</span></span>           | <span data-ttu-id="c011c-140">ฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="c011c-141">ผู้จัดการฝ่ายขาย</span><span class="sxs-lookup"><span data-stu-id="c011c-141">Sales manager</span></span> | <span data-ttu-id="c011c-142">ผู้จัดการระดับกลาง</span><span class="sxs-lookup"><span data-stu-id="c011c-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="c011c-143">นักบัญชี</span><span class="sxs-lookup"><span data-stu-id="c011c-143">Accountant</span></span>    | <span data-ttu-id="c011c-144">ผู้เชี่ยวชาญ</span><span class="sxs-lookup"><span data-stu-id="c011c-144">Professionals</span></span>        |

<span data-ttu-id="c011c-145">คุณสามารถรักษาฟังก์ชันงานได้ที่หน้า **ฟังก์ชันงาน**</span><span class="sxs-lookup"><span data-stu-id="c011c-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="c011c-146">บนหน้า **ฟังก์ชันงาน** ป้อนรหัสการระบุและคำอธิบายโดยย่อของฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="c011c-147">การปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-147">Job tasks</span></span>
<span data-ttu-id="c011c-148">การปฏิบัติงานอธิบายถึงงานพื้นฐานที่ผู้ปฏิบัติงานในตำแหน่งนั้นต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c011c-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="c011c-149">การปฏิบัติงานที่เหมือนกันสามารถเพิ่มลงในงานหลายงาน และในตำแหน่งสำหรับงานดังกล่าวที่จะใช้การปฏิบัติงานเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c011c-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="c011c-150">ตารางต่อไปนี้แสดงตัวอย่างของการปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c011c-151">งาน</span><span class="sxs-lookup"><span data-stu-id="c011c-151">Job</span></span></th>
<th><span data-ttu-id="c011c-152">การปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c011c-153">ผู้จัดการฝ่ายขาย</span><span class="sxs-lookup"><span data-stu-id="c011c-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="c011c-154"><strong>Perf-ตรวจสอบ</strong> – ตรวจสอบประสิทธิภาพ&#39;ของพนักงานขายแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="c011c-154"><strong>Perf-review</strong> – Review each salesperson&#39;s job performance.</span></span></li>
<li><span data-ttu-id="c011c-155"><strong>Abs-ตรวจสอบ</strong> – อนุมัติหรือปฏิเสธคำขอขาดงานหรือการลงทะเบียน&#39;ของพนักงานขายแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="c011c-155"><strong>Abs-review</strong> – Approve or reject each salesperson&#39;s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c011c-156">นักบัญชี</span><span class="sxs-lookup"><span data-stu-id="c011c-156">Accountant</span></span></td>
<td><span data-ttu-id="c011c-157"><strong>การรายงาน FIN</strong> – นำเสนอรายงานทางการเงินรายสัปดาห์ให้ประธานเจ้าหน้าที่ฝ่ายการเงิน</span><span class="sxs-lookup"><span data-stu-id="c011c-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c011c-158">คุณสามารถรักษาการปฏิบัติงานได้ที่หน้า **การปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="c011c-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="c011c-159">บนหน้า **การปฏิบัติงาน** ป้อนชื่อและคำอธิบายโดยย่อของการปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="c011c-160">ในฟิลด์ **หมายเหตุ** คุณสามารถเลือกป้อนข้อมูลเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="c011c-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="c011c-161">สามารถอัพเดตบันทึกย่อสำหรับงานหนึ่ง ๆ โดยไม่เปลี่ยนแปลงบันทึกย่อที่คุณป้อนที่นี่</span><span class="sxs-lookup"><span data-stu-id="c011c-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="c011c-162">ขอบเขตความรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="c011c-162">Areas of responsibility</span></span>
<span data-ttu-id="c011c-163">คุณใช้ขอบเขตความรับผิดชอบเพื่อระบุ บทบาทงาน กระบวนการ ผลิตภัณฑ์ ที่ผู้ปฏิบัติงานในตำแหน่งงานนั้นมีหน้าที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="c011c-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="c011c-164">ตัวอย่างเช่น สำหรับงานที่มีชื่อว่า "นักบัญชี" ความรับผิดชอบอย่างหนึ่งอาจเป็น "การรายงานการเงินสำหรับผลิตภัณฑ์ A"</span><span class="sxs-lookup"><span data-stu-id="c011c-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="c011c-165">คุณรักษาขอบเขตความรับผิดชอบได้ที่หน้า **พื้นที่ของความรับผิดชอบ** ซึ่งคุณสามารถค้นหาได้โดยใช้ฟังก์ชันการค้นหา</span><span class="sxs-lookup"><span data-stu-id="c011c-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="c011c-166">บนหน้า **ขอบเขตของความรับผิดชอบ** ป้อนชื่อและคำอธิบายโดยย่อของความรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="c011c-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="c011c-167">ในฟิลด์ **หมายเหตุ** คุณสามารถเลือกป้อนข้อมูลเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="c011c-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="c011c-168">สามารถอัพเดตบันทึกย่อสำหรับงานหนึ่ง ๆ โดยไม่เปลี่ยนแปลงบันทึกย่อที่คุณป้อนที่นี่</span><span class="sxs-lookup"><span data-stu-id="c011c-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="steps-for-creating-a-job"></a><span data-ttu-id="c011c-169">ขั้นตอนสำหรับการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="c011c-169">Steps for creating a job</span></span>
<span data-ttu-id="c011c-170">อ้างอิงถึงหัวข้อ [กำหนดงานใหม่](../fin-and-ops/hr/tasks/define-new-jobs.md) สำหรับกระบวนงานแบบเป็นขั้นตอนสำหรับการสร้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c011c-170">Refer to the [Define new jobs](../fin-and-ops/hr/tasks/define-new-jobs.md) topic for the step-by-step procedure for creating a new job.</span></span> 
