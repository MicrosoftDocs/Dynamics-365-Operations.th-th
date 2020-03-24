---
title: ใช้รายงานการวิเคราะห์ใน Attract
description: หัวข้อนี้อธิบายถึงรายงานการวิเคราะห์สำหรับข้อมูลเชิงลึกในกระบวนการจ้างงานใน Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092234"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="c66aa-103">ใช้รายงานการวิเคราะห์ใน Attract</span><span class="sxs-lookup"><span data-stu-id="c66aa-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c66aa-104">รายงานการวิเคราะห์ใน Microsoft Dynamics 365 Talent: Attract แบบสำเร็จรูปสำหรับข้อมูลเชิงลึกกระบวนการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="c66aa-105">คุณลักษณะที่พร้อมใช้งาน ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="c66aa-105">Availabe features include:</span></span>

- <span data-ttu-id="c66aa-106">**การวิเคราะห์งาน** คลิกแท็บ **การวิเคราะห์** ภายในงานสำหรับการวัดในผู้สมัครงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="c66aa-107">**ฮับการวิเคราะห์:** คลิก **การวิเคราะห์** บนการนำทางด้านซ้ายสำหรับการวัดรวมในงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="c66aa-108">**ความปลอดภัยเฉพาะผู้ใช้** มีการควบคุมการเข้าถึงรายงานโดย [บทบาท](security-attract.md) Attract และบทบาทผู้เข้าร่วมงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="c66aa-109">**การกรองไขว้** คลิกที่ภาพภายในรายงานเพื่อดูการวัดอื่นๆ ที่ถูกกรองโดยข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c66aa-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="c66aa-110">ในขณะนี้คุณลักษณะนี้อยู่ใน [การแสดงตัวอย่าง](access-preview-feature.md)</span><span class="sxs-lookup"><span data-stu-id="c66aa-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="c66aa-111">เมื่อต้องการลองใช้ คุณต้องมี [**Add-On การจ้างงานที่ครอบคลุม**](attract-comprehensive-hiring.md)</span><span class="sxs-lookup"><span data-stu-id="c66aa-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="c66aa-112">รายงานการแสดงตัวอย่างสาธารณะทั้งหมดจะถูกแสดงเป็นภาษาอังกฤษ</span><span class="sxs-lookup"><span data-stu-id="c66aa-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="c66aa-113">รายงานจะรีเฟรชทุกๆ 3 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c66aa-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="c66aa-114">เวลาในการรีเฟรชครั้งล่าสุด (ในเขตเวลาท้องถิ่น) จะอยู่ที่ด้านบนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="c66aa-115">เวลาในการรีเฟรชคือการประมาณ และแตกต่างกันไปตามปริมาณข้อมูลและโหลดทรัพยากรในภูมิภาคของคุณ</span><span class="sxs-lookup"><span data-stu-id="c66aa-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="c66aa-116">การวิเคราะห์งาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-116">Job Analytics</span></span>

<span data-ttu-id="c66aa-117">รายงานการวิเคราะห์งานคือสแนปช็อตของกระบวนการว่าจ้างสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="c66aa-118">การวัดที่สำคัญรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="c66aa-118">Key metrics include:</span></span>

- <span data-ttu-id="c66aa-119">ผู้สมัครที่ใช้งานอยู่ตามระยะ</span><span class="sxs-lookup"><span data-stu-id="c66aa-119">Active applicants by stage</span></span>
- <span data-ttu-id="c66aa-120">แหล่งที่มาของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="c66aa-120">Applicant source</span></span>
- <span data-ttu-id="c66aa-121">ชนิดของผู้สมัคร (ภายในหรือภายนอก)</span><span class="sxs-lookup"><span data-stu-id="c66aa-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="c66aa-122">ฮับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="c66aa-122">Analytics Hub</span></span>

<span data-ttu-id="c66aa-123">ฮับการวิเคราะห์รายงานข้อมูลรวมในงาน เพื่อแสดงแนวโน้มในกระบวนการว่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="c66aa-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="c66aa-124">Attract รวมรายงาน OOTB สองฉบับ: สรุปไปป์ไลน์และการวิเคราะห์แบบ Funnel</span><span class="sxs-lookup"><span data-stu-id="c66aa-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="c66aa-125">สรุปขั้นตอนการขาย</span><span class="sxs-lookup"><span data-stu-id="c66aa-125">Pipeline Summary</span></span>

<span data-ttu-id="c66aa-126">รายงานสรุปของไปป์ไลน์รวมข้อมูลสำหรับงานที่เปิดค้างไว้</span><span class="sxs-lookup"><span data-stu-id="c66aa-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="c66aa-127">การวัดที่สำคัญรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="c66aa-127">Key metrics include:</span></span>

- <span data-ttu-id="c66aa-128">ผู้สมัครในงานทั้งหมดตามลำดับขั้น</span><span class="sxs-lookup"><span data-stu-id="c66aa-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="c66aa-129">แหล่งที่มาของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="c66aa-129">Applicant source</span></span>
- <span data-ttu-id="c66aa-130">งานที่เปิดโดยเรียงตามระดับความอาวุโส</span><span class="sxs-lookup"><span data-stu-id="c66aa-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="c66aa-131">การวิเคราะห์แบบ Funnel</span><span class="sxs-lookup"><span data-stu-id="c66aa-131">Funnel Analysis</span></span>

<span data-ttu-id="c66aa-132">รายงานการวิเคราะห์แบบ Funnel รวมข้อมูลสำหรับงานที่ได้ปิดเป็นเติมข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="c66aa-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="c66aa-133">การวัดที่สำคัญรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="c66aa-133">Key metrics include:</span></span>

- <span data-ttu-id="c66aa-134">เวลาในการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="c66aa-134">Time to hire</span></span>
- <span data-ttu-id="c66aa-135">การวัดการแปลง (บนโฮเวอร์)</span><span class="sxs-lookup"><span data-stu-id="c66aa-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="c66aa-136">อัตราการยอมรับข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="c66aa-136">Offer acceptance rate</span></span>

<span data-ttu-id="c66aa-137">หมายเหตุ: สำหรับเวลาที่ถูกต้องมากที่สุดในการรายงานการจ้างงาน ขอแนะนำให้คุณดู [การจัดการข้อเสนอ](offer-setup.md) คุณลักษณะที่พร้อมใช้งานเป็นส่วนหนึ่งของ Add-On การจ้างงานที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="c66aa-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="c66aa-138">ลองวางเมาส์เหนือภาพสำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c66aa-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="c66aa-139">ตัวอย่างเช่น การวางเมาส์เหนือภาพ **ผู้สมัครที่ใช้งานอยู่** จะแสดงจำนวนวันเฉลี่ยในขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="c66aa-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="c66aa-140">การวิเคราะห์ข้อมูลนี้สามารถให้ความสำคัญกับข้อมูลเชิงลึกในการลดเวลาในการจ้างงาน และเปิดใช้งานผู้สรรหาเพื่อให้ความสำคัญกับวิธีในการลดเวลาที่ใช้ในแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="c66aa-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="c66aa-141">ความปลอดภัยเฉพาะผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c66aa-141">User-specific security</span></span>

<span data-ttu-id="c66aa-142">รายงาน Attract สามารถเข้าถึงได้สำหรับผู้ดูแลระบบ อ่านทั้งหมด ผู้สรรหา และผู้จัดการฝ่ายจ้าง [บทบาท](security-attract.md)</span><span class="sxs-lookup"><span data-stu-id="c66aa-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="c66aa-143">ผู้ใช้ที่ไม่ได้รับมอบหมายไม่สามารถเข้าถึงหน้ารายงานการวิเคราะห์ได้ (การวิเคราะห์งาน หรือฮับการวิเคราะห์)</span><span class="sxs-lookup"><span data-stu-id="c66aa-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="c66aa-144">รายงานการวิเคราะห์งานแสดงข้อมูลสำหรับงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c66aa-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="c66aa-145">รายงานฮับการวิเคราะห์รวมข้อมูลในงานทั้งหมดที่ผู้ใช้สามารถดูได้</span><span class="sxs-lookup"><span data-stu-id="c66aa-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="c66aa-146">ผู้ใช้ที่สามารถดูทั้งงานของฉันและงานทั้งหมดได้ในหน้างาน จะมีมุมมองเดียวกันที่พร้อมใช้งานในฮับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="c66aa-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="c66aa-147">ตัวกรองแบบข้าม</span><span class="sxs-lookup"><span data-stu-id="c66aa-147">Cross-filter</span></span>

<span data-ttu-id="c66aa-148">หนึ่งในคุณลักษณะที่ดีของ Power BI คือ วิธีการทั้งหมดที่ภาพบนหน้ารายงานเชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="c66aa-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="c66aa-149">ถ้าคุณเลือกจุดข้อมูลบนหนึ่งในภาพ ภาพอื่นๆ ทั้งหมดบนหน้าที่มีข้อมูลนั้นจะเปลี่ยนแปลง ซึ่งขึ้นอยู่กับการเลือกนั้น</span><span class="sxs-lookup"><span data-stu-id="c66aa-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="c66aa-150">เรียนรู้เพิ่มเติมและดูตัวอย่างใน [วิธีการที่ภาพกรองแบบข้ามซึ่งกันและกันในรายงาน Power BI](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)</span><span class="sxs-lookup"><span data-stu-id="c66aa-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="c66aa-151">ส่งออกไปที่ Excel</span><span class="sxs-lookup"><span data-stu-id="c66aa-151">Export to Excel</span></span>

<span data-ttu-id="c66aa-152">เมื่อต้องการดูข้อมูลรายงานใน Excel คุณสามารถคลิกที่เมนูตัวเลือก (สามจุด) บนภาพ และเลือก **ส่งออกข้อมูลพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="c66aa-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="c66aa-153">ข้อมูลที่ส่งออกจะส่งออกเป็นถูกกรองแล้ว โดยคำนึงถึงสิทธิ์ของผู้ใช้ใน Attract</span><span class="sxs-lookup"><span data-stu-id="c66aa-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="c66aa-154">สำหรับข้อมูลเพิ่มเติม ดู [ส่งออกข้อมูลจากการแสดงภาพ](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data)</span><span class="sxs-lookup"><span data-stu-id="c66aa-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
