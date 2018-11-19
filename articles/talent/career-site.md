---
title: "ฟังก์ชันไซต์การทำงานใน Attract"
description: "บทความนี้แสดงภาพรวมของฟังก์ชันการทำงานการเชื่อมต่อกับผู้สมัครใน Microsoft Dynamics 365 for Talent - Attract บทความนี้ยังอธิบายวิธีการตั้งค่าฟังก์ชันนี้อีกด้วย"
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: th-th
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="923d0-104">ฟังก์ชันไซต์การทำงานใน Attract</span><span class="sxs-lookup"><span data-stu-id="923d0-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="923d0-105">บทความนี้แสดงภาพรวมของฟังก์ชันการทำงานการเชื่อมต่อกับผู้สมัครใน Microsoft Dynamics 365 for Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="923d0-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="923d0-106">บทความนี้ยังอธิบายวิธีการตั้งค่าฟังก์ชันนี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="923d0-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="923d0-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="923d0-107">Overview</span></span>

<span data-ttu-id="923d0-108">Attract ให้ไซต์การทำงานหนึ่งไซต์สำหรับแต่ละสภาพแวดล้อมในผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="923d0-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="923d0-109">ตัวอย่างเช่น ถ้าองค์กรมีสภาพแวดล้อมการพัฒนาและการทดสอบ ไซต์การทำงานหนึ่งไซต์จะถูกเตรียมใช้งานสำหรับสภาพแวดล้อมการพัฒนา และไซต์การทำงานอีกหนึ่งไซต์จะถูกเตรียมใช้งานสำหรับสภาพแวดล้อมการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="923d0-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="923d0-110">ไซต์การทำงานแต่ละไซต์เป็นแบบ **แยกต่างหากทั้งหมด** และมีกลไกการรับรองความถูกต้องของตนเอง</span><span class="sxs-lookup"><span data-stu-id="923d0-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="923d0-111">งานและโพรไฟล์ผู้สมัครไม่ได้ใช้ร่วมกันระหว่างไซต์ทำงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="923d0-112">โดยค่าเริ่มต้น ไซต์การทำงานเป็นแบบสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="923d0-112">By default, the career site is public.</span></span> <span data-ttu-id="923d0-113">ดังนั้น ผู้สมัครสามารถดูงานทั้งหมดที่ทำเครื่องหมายเป็นภายนอกได้ โดยไม่ต้องเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="923d0-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="923d0-114">อย่างไรก็ตาม การดำเนินการอื่นๆ ทั้งหมดกำหนดให้ผู้สมัครต้องล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="923d0-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="923d0-115">การจัดการไซต์อาชีพ</span><span class="sxs-lookup"><span data-stu-id="923d0-115">Career site management</span></span>

<span data-ttu-id="923d0-116">รายการต่อไปนี้บนไซต์การทำงานจะถูกควบคุมโดยการตั้งค่า:</span><span class="sxs-lookup"><span data-stu-id="923d0-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="923d0-117">**ชื่อองค์กร:** ชื่อองค์กรปรากฏขึ้นบนแถบนำทางด้านบนของไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="923d0-118">โดยการเลือกชื่อองค์กร ผู้สมัครไปยังหน้าซึ่งแสดงรายการงานที่เปิดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="923d0-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="923d0-119">**โลโก้องค์กร:** รูปโลโก้ขององค์กรปรากฏขึ้นในด้านซ้ายบนของไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="923d0-120">โดยการเลือกรูปโลโก้ ผู้สมัครไปยังหน้าซึ่งแสดงรายการงานที่เปิดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="923d0-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="923d0-121">ในการตั้งค่าสำหรับชื่อองค์กรและโลโก้ ล็อกอินไปยัง Attract ในฐานะผู้ดูแลระบบ เลือก **ศูนย์การจัดการ** บนเมนู **การตั้งค่า** (สัญลักษณ์เกียร์) และจากนั้นเลือกแท็บ **ข้อมูลของบริษัท**</span><span class="sxs-lookup"><span data-stu-id="923d0-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="923d0-122">รูปโลโก้ที่ปรากฏบนไซต์การทำงานมีความสูงคงที่เป็น 20 พิกเซล (px)</span><span class="sxs-lookup"><span data-stu-id="923d0-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="923d0-123">รูปภาพที่คุณเพิ่มในศูนย์การจัดการจะถูกปรับขนาดให้พอดี</span><span class="sxs-lookup"><span data-stu-id="923d0-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="923d0-124">ดังนั้น โดยขึ้นอยู่กับรูปภาพ ความกว้างอาจเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="923d0-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="923d0-125">URL ไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-125">Career site URL</span></span>

<span data-ttu-id="923d0-126">เมื่อคุณ [ลงรายการบัญชีงานภายนอก](./Creating-jobs-Attract.md#postings) เป็นครั้งแรก คุณสามารถคัดลอกลิงค์ **สมัคร** จากใบสมัคร Attract ได้</span><span class="sxs-lookup"><span data-stu-id="923d0-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="923d0-127">URL สำหรับการเชื่อมโยงนี้จะอยู่ในรูปแบบต่อไปนี้: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="923d0-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="923d0-128">URL ของไซต์การทำงานเป็นสตริงย่อยของ URL **สมัคร**</span><span class="sxs-lookup"><span data-stu-id="923d0-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="923d0-129">ซึ่งประกอบด้วยข้อมูลทั้งหมดไปจนถึงชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="923d0-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="923d0-130">ดังนั้น สำหรับ URL **สมัคร** ก่อนหน้า URL ของไซต์การทำงานคือ `https://jobs.talent.dynamics.com/jobs/<company_name>/`</span><span class="sxs-lookup"><span data-stu-id="923d0-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="923d0-131">ตัวเลือกการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="923d0-131">Authentication options</span></span>

<span data-ttu-id="923d0-132">ผู้สมัครมีตัวเลือกการลงชื่อเข้าใช้ดังต่อไปนี้สำหรับไซต์การทำงาน Attract:</span><span class="sxs-lookup"><span data-stu-id="923d0-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="923d0-133">บัญชีส่วนตัว:</span><span class="sxs-lookup"><span data-stu-id="923d0-133">Personal account:</span></span>

    - <span data-ttu-id="923d0-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="923d0-134">LinkedIn</span></span>
    - <span data-ttu-id="923d0-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="923d0-135">Microsoft</span></span>
    - <span data-ttu-id="923d0-136">Google</span><span class="sxs-lookup"><span data-stu-id="923d0-136">Google</span></span>
    - <span data-ttu-id="923d0-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="923d0-137">Facebook</span></span>

- <span data-ttu-id="923d0-138">บัญชีที่ทำงานหรือที่โรงเรียน:</span><span class="sxs-lookup"><span data-stu-id="923d0-138">Work or school account:</span></span>

    - <span data-ttu-id="923d0-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="923d0-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="923d0-140">การลงชื่อเข้าใช้ของ Azure AD มีไว้สำหรับผู้สมัครภายในเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="923d0-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="923d0-141">ดังนั้น จะใช้ได้สำหรับผู้สมัครภายในที่ใช้ข้อมูลประจำตัว Azure AD ของบริษัทของพวกเขาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="923d0-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="923d0-142">ตัวอย่างเช่น ผู้สมัครที่ปัจจุปันเป็นพนักงาน Contoso Ltd ต้องการสมัครงานในบริษัทที่ไม่เกี่ยวข้อง ซึ่งคือ Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="923d0-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="923d0-143">ในกรณีนี้ การลงชื่อเข้าใช้จะไม่สำเร็จ หากพนักงานพยายามที่จะใช้ข้อมูลประจำตัว Azure AD ของเขาหรือเธอจากบริษัท Contoso ltd</span><span class="sxs-lookup"><span data-stu-id="923d0-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="923d0-144">สร้างและรักษาโฟรไฟล์</span><span class="sxs-lookup"><span data-stu-id="923d0-144">Create and maintain a profile</span></span>

<span data-ttu-id="923d0-145">หลังจากที่ผู้สมัครลงชื่อเข้าใช้ไปยังไซต์การทำงาน พวกเขาจะสามารถเลือก **โพรไฟล์ของฉัน** บนแถบนำทางด้านบนของหน้า เพื่อสร้างและรักษาโพรไฟล์ของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="923d0-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="923d0-146">โพรไฟล์รวมข้อมูลส่วนบุคคล ข้อมูลเกี่ยวกับประสบการณ์การทำงาน รายละเอียดการศึกษา เอกสาร ลิงค์ และข้อมูลเกี่ยวกับชุดทักษะ</span><span class="sxs-lookup"><span data-stu-id="923d0-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="923d0-147">หลังจากที่มีการสร้างโพรไฟล์ ก็จะสามารถใช้เพื่อสมัครงานที่ผู้สมัครมีความสนใจได้</span><span class="sxs-lookup"><span data-stu-id="923d0-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="923d0-148">โพรไฟล์ยังช่วย Attract แนะนำงานที่ถูกต้องให้กับผู้สมัครได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="923d0-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="923d0-149">ค้นหางานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="923d0-149">Find the right job</span></span>

<span data-ttu-id="923d0-150">บนหน้ารายการงาน ผู้สมัครสามารถค้นหางานเฉพาะ โดยการป้อนเงื่อนไขการค้นหา</span><span class="sxs-lookup"><span data-stu-id="923d0-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="923d0-151">ฟังก์ชันการค้นหาจะค้นหาเงื่อนไขการค้นหาในตำแหน่งงานและคำอธิบายเกี่ยวกับงาน และแสดงงานที่เกี่ยวข้องเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="923d0-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="923d0-152">ผู้สมัครสามารถกรองผลลัพธ์ได้ตลอดเวลา โดยขึ้นอยู่กับตำแหน่งงานหรือฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="923d0-153">ผู้สมัครยังสามารถดูชุดของงานที่แนะนำได้บนไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="923d0-154">งานที่แนะนำให้ผู้สมัครขึ้นอยู่กับใบสมัครที่ผ่านมาของผู้สมัคร โพรไฟล์ และประวัติย่อ</span><span class="sxs-lookup"><span data-stu-id="923d0-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="923d0-155">มีการแสดงคำแนะนำเกี่ยวกับงาน ก็ต่อเมื่อมีการลงรายการบัญชีงานอย่างน้อย 10 งานบนไซต์การทำงาน และเมื่อผู้สมัครได้กรอกข้อมูลโพรไฟล์ของเขาหรือเธอเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="923d0-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="923d0-156">สมัครงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-156">Apply for jobs</span></span>

<span data-ttu-id="923d0-157">หลังจากที่ผู้สมัครพบงานที่เหมาะสม พวกเขาสามารถสมัครได้โดยใช้ปุ่ม **สมัคร** บนหน้ารายละเอียดงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="923d0-158">ณ จุดนี้ ผู้สมัครสามารถสร้างโพรไฟล์ใหม่ หรือตรวจทานข้อมูลในโพรไฟล์ที่มีอยู่ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="923d0-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="923d0-159">ผู้สมัครยังสามารถอัพโหลดประวัติย่อได้ตามความจำเป็น แล้วจากนั้น ส่งใบสมัครงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="923d0-160">ตรวจสอบสถานะใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="923d0-160">Check application status</span></span>

<span data-ttu-id="923d0-161">หลังจากที่ผู้สมัครสมัครอย่างน้อยหนึ่งงาน พวกเขาจะสามารถเลือก **ใบสมัคร** บนแถบนำทางด้านบนของหน้า เพื่อดูใบสมัครที่เปิดและปิดของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="923d0-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="923d0-162">เมื่อผู้สมัครเปิดหนึ่งในใบสมัครของพวกเขา พวกเขาจะเห็นขั้นปัจจุบันและรายการการดำเนินการใดๆ ที่ค้างอยู่ ที่พวกเขาต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="923d0-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="923d0-163">ตัวอย่างเช่น ถ้าผู้สมัครต้องระบุวันที่เป็นไปได้สำหรับการสัมภาษณ์ส่วนบุคคล หน้าจะแสดงตัวเลือกของเขาหรือเธอ</span><span class="sxs-lookup"><span data-stu-id="923d0-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="923d0-164">งานภายใน</span><span class="sxs-lookup"><span data-stu-id="923d0-164">Internal jobs</span></span>

<span data-ttu-id="923d0-165">ในปัจจุบัน งานที่ถูกทำเครื่องหมายเป็นภายใน และลงรายการบัญชีไปยังไซต์การทำงาน Attract ไม่ปรากฏบนไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="923d0-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="923d0-166">พวกเขาสามารถเข้าถึงได้โดยผ่านทาง URL **สมัคร** โดยตรง ที่คุณสามารถคัดลอกจากใบสมัคร Attract ได้</span><span class="sxs-lookup"><span data-stu-id="923d0-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

