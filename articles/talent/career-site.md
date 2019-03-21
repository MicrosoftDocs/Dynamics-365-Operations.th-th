---
title: ฟังก์ชันไซต์การทำงานใน Attract
description: หัวข้อนี้แสดงภาพรวมของฟังก์ชันไซต์การทำงานที่เชื่อมต่อกับผู้สมัครใน Attract
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/13/2019
ms.locfileid: "389988"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="813a6-103">ฟังก์ชันไซต์การทำงานใน Attract</span><span class="sxs-lookup"><span data-stu-id="813a6-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="813a6-104">หัวข้อนี้แสดงภาพรวมของฟังก์ชันไซต์การทำงานที่เชื่อมต่อกับผู้สมัครใน Microsoft Dynamics 365 for Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="813a6-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="813a6-105">นอกจากนี้ ยังอธิบายวิธีการตั้งค่าฟังก์ชันนี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="813a6-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="813a6-106">Attract ให้ไซต์การทำงานหนึ่งไซต์สำหรับแต่ละสภาพแวดล้อมในผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="813a6-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="813a6-107">ตัวอย่างเช่น ถ้าองค์กรมีสภาพแวดล้อมการพัฒนาและสภาพแวดล้อมการทดสอบ ไซต์การทำงานหนึ่งไซต์จะถูกเตรียมใช้งานสำหรับสภาพแวดล้อมการพัฒนา และไซต์การทำงานอีกหนึ่งไซต์จะถูกเตรียมใช้งานสำหรับสภาพแวดล้อมการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="813a6-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="813a6-108">ไซต์การทำงานแต่ละไซต์เป็นแบบแยกต่างหากทั้งหมด และมีกลไกการรับรองความถูกต้องของตนเอง</span><span class="sxs-lookup"><span data-stu-id="813a6-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="813a6-109">งานและโพรไฟล์ผู้สมัครไม่ได้ใช้ร่วมกันระหว่างไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="813a6-110">โดยค่าเริ่มต้น ไซต์การทำงานเป็นแบบสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="813a6-110">By default, the career site is public.</span></span> <span data-ttu-id="813a6-111">ดังนั้น ผู้สมัครสามารถดูงานทั้งหมดที่ทำเครื่องหมายเป็นภายนอกได้ โดยไม่ต้องเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="813a6-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="813a6-112">อย่างไรก็ตาม การดำเนินการอื่นๆ ทั้งหมดกำหนดให้ผู้สมัครต้องเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="813a6-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="813a6-113">การจัดการไซต์อาชีพ</span><span class="sxs-lookup"><span data-stu-id="813a6-113">Career site management</span></span>

<span data-ttu-id="813a6-114">ในการตั้งค่าสำหรับรายการต่อไปนี้ ล็อกอินไปยัง Attract ในฐานะผู้ดูแลระบบ เลือก **ศูนย์การจัดการ** บนเมนู **การตั้งค่า** (สัญลักษณ์เกียร์) และจากนั้นเลือกแท็บ **ข้อมูลของบริษัท**</span><span class="sxs-lookup"><span data-stu-id="813a6-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="813a6-115">**ชื่อองค์กร:** - ชื่อองค์กรปรากฏขึ้นบนแถบนำทางด้านบนของไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="813a6-116">โดยการเลือกชื่อองค์กร ผู้สมัครไปยังหน้าซึ่งแสดงรายการงานที่เปิดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="813a6-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="813a6-117">**โลโก้องค์กร:** - รูปโลโก้ขององค์กรปรากฏขึ้นในด้านซ้ายบนของไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="813a6-118">โดยการเลือกรูปโลโก้ ผู้สมัครไปยังหน้าซึ่งแสดงรายการงานที่เปิดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="813a6-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="813a6-119">รูปโลโก้ที่ปรากฏบนไซต์การทำงานมีความสูงคงที่เป็น 20 พิกเซล (px)</span><span class="sxs-lookup"><span data-stu-id="813a6-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="813a6-120">รูปภาพที่คุณเพิ่มในศูนย์การจัดการจะถูกปรับขนาดให้พอดี</span><span class="sxs-lookup"><span data-stu-id="813a6-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="813a6-121">ดังนั้น โดยขึ้นอยู่กับรูปภาพ ความกว้างอาจเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="813a6-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="813a6-122">ในการตั้งค่าสำหรับรายการต่อไปนี้ ล็อกอินไปยัง Attract ในฐานะผู้ดูแลระบบ เลือก **ศูนย์การจัดการ** บนเมนู **การตั้งค่า** (สัญลักษณ์เกียร์) และจากนั้นเลือกแท็บ **การจัดการไซต์อาชีพ**</span><span class="sxs-lookup"><span data-stu-id="813a6-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="813a6-123">**การเพิ่มประสิทธิภาพกลไกจัดการการค้นหา** - เมื่อเปิดใช้งาน งานสาธารณะทั้งหมดที่ลงรายการบัญชีไซต์การทำงาน Attract จะถูกค้นหา โดยใช้โปรแกรมค้นหา เช่น Bing และ Google</span><span class="sxs-lookup"><span data-stu-id="813a6-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="813a6-124">อาจมีความล่าช้าระหว่างการเปิดใช้การตั้งค่านี้และผลการค้นหาที่ปรากฏ โดยขึ้นอยู่กับโปรแกรมค้นหาที่คุณกำลังใช้</span><span class="sxs-lookup"><span data-stu-id="813a6-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="813a6-125">URL ไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-125">Career site URLs</span></span>

<span data-ttu-id="813a6-126">รายการต่อไปนี้ประกอบด้วย URL ของไซต์การทำงานที่ใช้กันทั่วไปและวิธีการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="813a6-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="813a6-127">**URL โฮมเพจของไซต์การทำงาน** - เมื่อต้องการดู URL โฮมเพจของไซต์การทำงาน ล็อกอินไปยัง Attract ในฐานะผู้ดูแลระบบ เลือก **ศูนย์การจัดการ** บนเมนู **การตั้งค่า** และจากนั้นเลือกแท็บ **การจัดการไซต์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="813a6-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="813a6-128">**URL การสมัครโพสต์งานแต่ละรายการ** - [เมื่อคุณโพสต์งานภายนอก](Creating-jobs-Attract.md#postings) เป็นครั้งแรก คุณสามารถคัดลอกลิงค์ **สมัคร** จากใบสมัคร Attract ได้</span><span class="sxs-lookup"><span data-stu-id="813a6-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="813a6-129">URL สำหรับการเชื่อมโยงนี้จะอยู่ในรูปแบบต่อไปนี้: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="813a6-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="813a6-130">**URL ของโพสต์งานแต่ละรายการ** - URL ของโพสต์งานเป็นสตริงย่อยของ URL การสมัคร</span><span class="sxs-lookup"><span data-stu-id="813a6-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="813a6-131">ซึ่งประกอบด้วยข้อมูลทั้งหมดไปจนถึงหมายเลขงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="813a6-132">ดังนั้น สำหรับ URL การสมัครก่อนหน้า URL ของโพสต์งานคือ [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="813a6-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="813a6-133">ตัวเลือกการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="813a6-133">Authentication options</span></span>

<span data-ttu-id="813a6-134">ผู้สมัครมีตัวเลือกการลงชื่อเข้าใช้ดังต่อไปนี้สำหรับไซต์การทำงาน Attract:</span><span class="sxs-lookup"><span data-stu-id="813a6-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="813a6-135">บัญชีส่วนตัว:</span><span class="sxs-lookup"><span data-stu-id="813a6-135">Personal account:</span></span>

    -   <span data-ttu-id="813a6-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="813a6-136">LinkedIn</span></span>

    -   <span data-ttu-id="813a6-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="813a6-137">Microsoft</span></span>

    -   <span data-ttu-id="813a6-138">Google</span><span class="sxs-lookup"><span data-stu-id="813a6-138">Google</span></span>

    -   <span data-ttu-id="813a6-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="813a6-139">Facebook</span></span>

-   <span data-ttu-id="813a6-140">บัญชีที่ทำงานหรือที่โรงเรียน:</span><span class="sxs-lookup"><span data-stu-id="813a6-140">Work or school account:</span></span>

    -   <span data-ttu-id="813a6-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="813a6-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="813a6-142">การลงชื่อเข้าใช้ของ Azure AD มีไว้สำหรับผู้สมัครภายในเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="813a6-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="813a6-143">ดังนั้น จะใช้ได้สำหรับผู้สมัครภายในที่ใช้ข้อมูลประจำตัว Azure AD ของบริษัทของพวกเขาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="813a6-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="813a6-144">ตัวอย่างเช่น ผู้สมัครที่ปัจจุปันเป็นพนักงานของ Contoso Ltd ต้องการสมัครงานในบริษัทที่ไม่เกี่ยวข้อง ซึ่งคือ Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="813a6-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="813a6-145">ในกรณีนี้ การลงชื่อเข้าใช้จะไม่สำเร็จ หากพนักงานพยายามที่จะใช้ข้อมูลประจำตัว Azure AD ของเขาหรือเธอจากบริษัท Contoso ltd</span><span class="sxs-lookup"><span data-stu-id="813a6-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="813a6-146">สร้างและรักษาโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="813a6-146">Create and maintain a profile</span></span>

<span data-ttu-id="813a6-147">หลังจากที่ผู้สมัครลงชื่อเข้าใช้ไปยังไซต์การทำงาน พวกเขาจะสามารถเลือก **โพรไฟล์ของฉัน** บนแถบนำทางที่ด้านบนของหน้า เพื่อสร้างและรักษาโพรไฟล์ของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="813a6-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="813a6-148">โพรไฟล์รวมข้อมูลส่วนบุคคล ข้อมูลเกี่ยวกับประสบการณ์การทำงาน รายละเอียดการศึกษา เอกสาร ลิงค์ และข้อมูลเกี่ยวกับชุดทักษะ</span><span class="sxs-lookup"><span data-stu-id="813a6-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="813a6-149">หลังจากที่มีการสร้างโพรไฟล์ ก็จะสามารถใช้เพื่อสมัครงานที่ผู้สมัครมีความสนใจได้</span><span class="sxs-lookup"><span data-stu-id="813a6-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="813a6-150">โพรไฟล์ยังช่วย Attract แนะนำงานที่เหมาะสมให้กับผู้สมัครได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="813a6-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="813a6-151">ถ้าผู้สมัครใช้รหัสอีเมลเพื่อล็อกอิน โดยใช้หนึ่งในตัวให้บริการการรับรองความถูกต้องที่แสดงรายการข้างต้น รหัสอีเมลนั้นจะมีค่าเริ่มต้นเป็นรหัสอีเมลของผู้ติดต่อที่เชื่อมโยงกับโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="813a6-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="813a6-152">อย่างไรก็ตาม จะสามารถเปลี่ยนได้ตลอดเวลา และเป็นอิสระโดยสิ้นเชิงจากของเดิม</span><span class="sxs-lookup"><span data-stu-id="813a6-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="813a6-153">Attract จะใช้รหัสอีเมลของผู้ติดต่อเสมอ เพื่อเชื่อมโยงกับโพรไฟล์ของคุณสำหรับการสื่อสารทางอีเมลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="813a6-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="813a6-154">ค้นหางานที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="813a6-154">Find the right job</span></span>

<span data-ttu-id="813a6-155">บนหน้ารายการงาน ผู้สมัครสามารถค้นหางานเฉพาะได้โดยการป้อนเงื่อนไขการค้นหา</span><span class="sxs-lookup"><span data-stu-id="813a6-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="813a6-156">ฟังก์ชันการค้นหาจะค้นหาเงื่อนไขการค้นหาในตำแหน่งงานและคำอธิบายเกี่ยวกับงาน และแสดงงานที่เกี่ยวข้องเป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="813a6-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="813a6-157">ผู้สมัครสามารถกรองผลลัพธ์ได้ตลอดเวลา โดยขึ้นอยู่กับตำแหน่งงานหรือฟังก์ชันงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="813a6-158">ผู้สมัครยังสามารถดูชุดของงานที่แนะนำได้บนไซต์การทำงานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="813a6-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="813a6-159">งานที่แนะนำให้ผู้สมัครขึ้นอยู่กับใบสมัคร โพรไฟล์ และประวัติย่อ ที่ผ่านมาของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="813a6-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="813a6-160">มีการแสดงคำแนะนำเกี่ยวกับงาน ก็ต่อเมื่อมีการลงรายการบัญชีงานอย่างน้อย 10 งานบนไซต์การทำงาน และเมื่อผู้สมัครได้กรอกข้อมูลโพรไฟล์เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="813a6-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="813a6-161">สมัครงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-161">Apply for jobs</span></span>

<span data-ttu-id="813a6-162">หลังจากที่ผู้สมัครพบงานที่เหมาะสม พวกเขาสามารถสมัครได้โดยใช้ปุ่ม **สมัคร** บนหน้า **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="813a6-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="813a6-163">ณ จุดนี้ ผู้สมัครสามารถสร้างโพรไฟล์ใหม่ หรือตรวจทานข้อมูลในโพรไฟล์ที่มีอยู่ของพวกเขาได้ อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="813a6-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="813a6-164">ผู้สมัครยังสามารถอัพโหลดประวัติย่อได้ตามความจำเป็น แล้วจากนั้น ส่งใบสมัครงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="813a6-165">ตรวจสอบสถานะใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="813a6-165">Check application status</span></span>

<span data-ttu-id="813a6-166">หลังจากที่ผู้สมัครสมัครงานอย่างน้อยหนึ่งงาน พวกเขาจะสามารถเลือก **ใบสมัคร** บนแถบนำทางที่ด้านบนของหน้า เพื่อดูใบสมัครที่เปิดและปิดของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="813a6-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="813a6-167">เมื่อผู้สมัครเปิดหนึ่งในใบสมัครของพวกเขา พวกเขาจะเห็นขั้นตอนปัจจุบันและรายการการดำเนินการใดๆ ที่ค้างอยู่ ที่พวกเขาต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="813a6-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="813a6-168">ตัวอย่างเช่น ถ้าผู้สมัครต้องระบุวันที่ที่เป็นไปได้สำหรับการสัมภาษณ์ส่วนบุคคล หน้าจะแสดงตัวเลือกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="813a6-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="813a6-169">งานภายใน</span><span class="sxs-lookup"><span data-stu-id="813a6-169">Internal jobs</span></span>

<span data-ttu-id="813a6-170">ในปัจจุบัน งานที่ถูกทำเครื่องหมายเป็นภายใน และถูกลงรายการบัญชีไปยังไซต์การทำงาน Attract ไม่ปรากฏบนไซต์การทำงาน</span><span class="sxs-lookup"><span data-stu-id="813a6-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="813a6-171">รายการเหล่านั้นสามารถเข้าถึงได้โดยใช้ทาง URL **สมัคร** โดยตรง ที่คุณสามารถคัดลอกจากใบสมัคร Attract ได้</span><span class="sxs-lookup"><span data-stu-id="813a6-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
