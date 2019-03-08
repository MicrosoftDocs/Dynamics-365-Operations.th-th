---
title: การจัดหาที่มีผู้สรรหาบุคลากร LinkedIn
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการใช้ Machine Learning ในการรับงานและคำแนะนำของผู้สมัครงาน
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306371"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="99d5d-103">การจัดหาที่มีผู้สรรหาบุคลากร LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="99d5d-104">LinkedIn เป็นฐานข้อมูล talent ที่ใหญ่ที่สุดในโลก และเป็นระบบหลักที่ผู้สรรหามักใช้ในการค้นหา สื่อสารกับ และจัดหาผู้สมัคร สำหรับงานที่ผู้สรรหากำลังมองหาเพื่อเติมเต็ม</span><span class="sxs-lookup"><span data-stu-id="99d5d-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="99d5d-105">การรวมผู้สรรหา LinkedIn กับ Dynamics 365 for Talent: Attract ทำให้ง่ายขึ้นสำหรับผู้ใช้ในการว่าจ้าง และเพื่อเก็บข้อมูลให้ตรงกันระหว่างสองระบบ</span><span class="sxs-lookup"><span data-stu-id="99d5d-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="99d5d-106">คุณต้องการ Add-On การจ้างงานแบบครอบคลุม และสิทธิ์การใช้งานของผู้สรรหา LinkedIn ให้สามารถใช้การรวมผู้สรรหา LinkedIn กับ Attract ได้</span><span class="sxs-lookup"><span data-stu-id="99d5d-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="99d5d-107">ตั้งค่าผู้สรรหา LinkedIn กับ Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="99d5d-108">ก่อนที่คุณจะสามารถใช้ความสามารถของผู้สรรหา LinkedIn ได้ คุณต้องตั้งค่าคอนฟิกการเข้าถึงระดับสัญญา หรือระดับบริษัท กับอินสแตนซ์ Attract ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99d5d-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="99d5d-109">เมื่อต้องการดำเนินการขั้นตอนการตั้งค่าคอนฟิกให้เสร็จสมบูรณ์ คุณต้องทำงานกับผู้ใช้ที่เป็นผู้ดูแลระบบในสัญญาผู้สรรหา LinkedIn ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99d5d-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="99d5d-110">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ เพื่อตั้งค่าคอนฟิกผู้สรรหา LinkedIn กับ Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="99d5d-111">ลงชื่อเข้าใช้ไปยัง Attract ในฐานะผู้ดูแลระบบ และไปยัง **การตั้งค่าผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="99d5d-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="99d5d-112">บนบานหน้าต่างด้านซ้าย ให้คลิกแท็บ **การรวม LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="99d5d-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="99d5d-113">[![มุมมองผู้ดูแลระบบ Attract เพื่อเริ่มต้นการรวมผู้สรรหา LinkedIn](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="99d5d-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="99d5d-114">คลิก **เชือมต่อ** เพื่อเริ่มต้นการตั้งค่า และรับคำแนะนำตลอดกระบวนการการเข้าสู่ระบบ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="99d5d-115">ถ้าคุณมีสิทธิ์การใช้งานในสัญญา LinkedIn หลายรายการ เลือกสัญญาที่คุณต้องการให้เชื่อมต่อกับระบบ Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="99d5d-116">ถ้าคุณสิทธิ์การใช้งานในสัญญา LinkedIn เพียงรายการเดียวเท่านั้น ขั้นตอนนี้ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="99d5d-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="99d5d-117">ขณะนี้ วิดเจ็ต LinkedIn จะโหลดในการตั้งค่าผู้ดูแลระบบของคุณด้วยรายการของการรวมที่แสดง</span><span class="sxs-lookup"><span data-stu-id="99d5d-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="99d5d-118">ภายใต้ **การเชื่อมต่อระบบผู้สรรหา** คลิก **ร้องขอ**</span><span class="sxs-lookup"><span data-stu-id="99d5d-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="99d5d-119">[![มุมมองผู้ดูแลระบบ Attract เพื่อร้องขอการรวมผู้สรรหา LinkedIn](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="99d5d-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="99d5d-120">หลังจากมีการร้องขอการรวมจาก Attract จะแสดงเป็น **คู่ค้าพร้อม** และพร้อมที่จะเปิดใช้งานจาก **การตั้งค่าผู้ดูแลระบบผู้สรรหา**</span><span class="sxs-lookup"><span data-stu-id="99d5d-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="99d5d-121">ถ้าคุณเห็น **แจ้งให้คู่ค้าทราบ** บนหน้านี้ ให้รอสักครู่ คลิก **แจ้งให้คู่ค้าทราบ** แล้วรีเฟรชหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="99d5d-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="99d5d-122">ขณะนี้ จึงควรแสดงเป็น **คู่ค้าพร้อม**</span><span class="sxs-lookup"><span data-stu-id="99d5d-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="99d5d-123">[![มุมมองผู้ดูแลระบบ Attract เพื่อบ่งชี้ฝั่ง Attract ของคำขอได้ถูกดำเนินการเสร็จสมบูรณ์แล้ว](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="99d5d-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="99d5d-124">เพื่อดำเนินการให้ขั้นตอนถัดไปเสร็จสิ้น คุณต้องมีสิทธิ์ผู้ดูแลระบบบนสัญญาผู้สรรหา LinkedIn ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99d5d-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="99d5d-125">ลงชื่อเข้าใช้ไปยัง LinkedIn โดยใช้บัญชีผู้ดูแลระบบ และไปยังผู้สรรหา LinkedIn ที่ด้านขวาบน</span><span class="sxs-lookup"><span data-stu-id="99d5d-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="99d5d-126">ในเมนู **เพิ่มเติม** ที่ด้านบนของหน้าจอ คลิก **การตั้งค่าผู้ดูแลระบบ** แล้วคลิกแท็บ **ATS**</span><span class="sxs-lookup"><span data-stu-id="99d5d-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="99d5d-127">ระบบ Attract จะถูกแสดงรายการ ด้วยตัวเลือกสองตัวเลือกที่สามารถเปิดได้</span><span class="sxs-lookup"><span data-stu-id="99d5d-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="99d5d-128">ถ้าคุณต้องการเปิดใช้งานการส่งออกแบบคลิกเพียงครั้ง 1 สำหรับ **ตัวบ่งชี้ In-ATS** และ **วิดเจ็ตโพรไฟล์ In-ATS** เลือก **การเข้าถึงระดับบริษัท**</span><span class="sxs-lookup"><span data-stu-id="99d5d-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="99d5d-129">ถ้าคุณต้องการเปิดใช้งานคุณลักษณะการเข้าถึงระดับบริษัททั้งหมด รวมทั้งประวัติ InMail ประวัติบันทึกย่อ และการเข้าถึงโปรไฟล์ส่วนที่เหลือของ InMail เลือก **การเข้าถึงระดับสัญญา**</span><span class="sxs-lookup"><span data-stu-id="99d5d-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="99d5d-130">เปิดใช้งานระดับการเข้าถึงที่ต้องการจากการตั้งค่า **Admin ATS** ของผู้สรรหา LinkedIn ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99d5d-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="99d5d-131">[![เปิดการรวม Attract จากมุมมองผู้ดูแลระบบของผู้สรรหา LinkedIn](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="99d5d-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="99d5d-132">ไปกลับยังการตั้งค่าของผู้ดูแลระบบ Attract ในฐานะ AttractAdmin และเลือกแท็บ **การรวม LinkedIn** ขณะนี้ คุณควรเห็นการโหลดวิดเจ็ต LinkedIn ที่แสดงว่า **ถูกเปิดใช้งาน** กับระดับการเข้าถึงที่เลือกไว้เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="99d5d-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="99d5d-133">[![การรวมผู้สรรหา LinkedIn เสร็จสมบูรณ์](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="99d5d-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="99d5d-134">การใช้ความสามารถของผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="99d5d-135">หลังจากที่มีการเปิดใช้ความสามารถของผู้สรรหา LinkedIn โดยผู้ดูแลระบบ Attract จึงพร้อมใช้งานสำหรับผู้จัดการว่าจ้างและผู้สรรหาในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="99d5d-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="99d5d-136">เพื่อใช้ความสามารถนี้ เชื่อมโยงบัญชี LinkedIn ของคุณภายใต้ **การตั้งค่าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="99d5d-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="99d5d-137">ความสามารถต่างๆ จะพร้อมใช้งาน หลังจากที่มีการเชื่อมต่อทั้งการตั้งค่าผู้ดูแลระบบและผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="99d5d-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="99d5d-138">วิดเจ็ตโพรไฟล์ In-ATS</span><span class="sxs-lookup"><span data-stu-id="99d5d-138">In-ATS profile widget</span></span>

<span data-ttu-id="99d5d-139">คุณสามารถดูโพรไฟล์ LinkedIn ของผู้สมัครได้ใน Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="99d5d-140">วิดเจ็ต LinkedIn จะแสดงโพรไฟล์ผู้สมัคร เมื่อข้อมูล ATS ตรงกับข้อมูล LinkedIn ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="99d5d-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="99d5d-141">เมื่อต้องการดูโพรไฟล์ ไปที่โพรไฟล์ผู้สมัครจากงานหรือกลุ่ม talent อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="99d5d-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="99d5d-142">ในโพรไฟล์ผู้สมัคร เลือกแท็บ **LinkedIn** และวิดเจ็ตโพรไฟล์จะโหลด</span><span class="sxs-lookup"><span data-stu-id="99d5d-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="99d5d-143">คุณยังสามารถบันทึกผู้สมัครไปยังโครงการผู้สรรหา LinkedIn ของคุณจากหน้านี้ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="99d5d-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="99d5d-144">ถ้า LinkedIn พบคู่ที่เป็นไปตามอีเมลและรหัสสมาชิก LinkedIn (ตรงกันทุกประการ) จะมีการแสดงโพรไฟล์ของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="99d5d-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="99d5d-145">นอกจากนี้ ผู้ใช้ยังมีตัวเลือกในการเชื่อมโยง/ยกเลิกเชื่อมโยงโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="99d5d-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="99d5d-146">ถ้า LinkedIn ไม่พบผู้สมัครตาม ID อีเมลหรือสมาชิก จะแสดงรายการของผู้สมัครที่เป็นไปได้ที่ตรงกันตามชื่อผู้สมัคร และผู้ใช้สามารถเลือกหนึ่งในรายการเท่านั้น และเชื่อมโยงโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="99d5d-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="99d5d-147">ถ้า LinkedIn ไม่พบผู้สมัครใดๆ ตามชื่อ จะแสดงค่าย้อนกลับว่า ไม่พบการจับคู่</span><span class="sxs-lookup"><span data-stu-id="99d5d-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="99d5d-148">การส่งออกด้วยการคลิก 1 ครั้ง</span><span class="sxs-lookup"><span data-stu-id="99d5d-148">1-click export</span></span> 

<span data-ttu-id="99d5d-149">ขณะจัดหาผู้สมัครใน LinkedIn คุณสามารถส่งออกผู้สมัครด้วยการคลิก 1 ครั้งไปยังงานที่คุณเปิดอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="99d5d-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="99d5d-150">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์สำหรับการส่งออกด้วยการคลิก 1 ครั้ง</span><span class="sxs-lookup"><span data-stu-id="99d5d-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="99d5d-151">ก่อนที่คุณจะดำเนินการขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ตรวจสอบว่าคุณได้รับกำหนดบทบาทของผู้จัดการว่าจ้าง หรือผู้สรรหาสำหรับงาน และงานมีขั้น **ผู้ที่มีแนวโน้มจะเป็นลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="99d5d-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="99d5d-152">สร้างงาน กำหนดบทบาทที่เหมาะสม และเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="99d5d-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="99d5d-153">เมื่อเรียกใช้งาน นำทางไปยังผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="99d5d-154">ค้นหาผู้สมัครที่คุณกำลังค้นหา และไปที่โพรไฟล์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="99d5d-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="99d5d-155">โดยใช้กล่องค้นหางานในบัตรผู้ติดต่อ หางานโดยใช้ตำแหน่งหรือรหัสงานที่ถูกเรียกใช้ใน Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="99d5d-156">ถ้าคุณไม่พบงาน คลิก **เปลี่ยน ATS** เพื่อพบอินสแตนซ์ Attract ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="99d5d-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="99d5d-157">หลังจากที่มีการเลือกงาน คลิก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="99d5d-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="99d5d-158">ขณะนี้ มีการนำผู้สมัครมาใช้โดย Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="99d5d-159">ไปที่ Attract และเปิดงานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="99d5d-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="99d5d-160">คุณจะพบผู้สมัครที่คุณเพิ่งส่งออกในขั้นของงาน **ผู้ที่มีแนวโน้มจะเป็นลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="99d5d-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="99d5d-161">ตัวบ่งชี้ In-ATS</span><span class="sxs-lookup"><span data-stu-id="99d5d-161">In-ATS indicator</span></span> 

<span data-ttu-id="99d5d-162">การใช้ผู้สรรหา LinkedIn คุณสามารถติดตามว่ามีใช้มีผลต่องานอื่นๆ ในองค์กรของคุณ ดูที่อยู่ในขั้นต่างๆ ของใบสมัครงาน และดูข้อคิดเห็นและข้อคิดเห็นจาก Attract ในผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="99d5d-163">เปิดผู้สรรหา LinkedIn และค้นหาโพรไฟล์ของผู้สมัครที่คุณกำลังค้นหา</span><span class="sxs-lookup"><span data-stu-id="99d5d-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="99d5d-164">เลื่อนลงไปดูส่วน **In-ATS** ในโพรไฟล์ของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="99d5d-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="99d5d-165">คุณสามารถใช้วิดเจ็ตนี้เพื่อดูข้อมูลทั้งหมดเกี่ยวกับผู้สมัครที่มีใน Attract จากภายในมุมมองผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="99d5d-166">เลือกแท็บ **งานและสถานะ** เพื่อดูงานที่พวกเขามีส่วนร่วม สถานะล่าสุด และวิธีที่พวกเขาได้เคลื่อนที่โดยเทียบกับแต่ละงาน</span><span class="sxs-lookup"><span data-stu-id="99d5d-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="99d5d-167">เลือกแท็บ **ผลป้อนกลับการสัมภาษณ์** เพื่อดูผลป้อนกลับที่ผู้สัมภาษณ์ส่งใน Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="99d5d-168">เลือกแท็บ **บันทึกย่อ** เพื่อดูบันทึกย่อที่มีการรวบรวมสำหรับผู้สมัครนี้ใน Attract</span><span class="sxs-lookup"><span data-stu-id="99d5d-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="99d5d-169">ข้อมูลผู้สมัครและใบสมัครจะไม่ถูกทำให้ข้อมูลตรงกับผู้สรรหา LinkedIn ถ้าผู้สมัครไม่ได้ย้ายผ่านขั้นผู้ที่มีแนวโน้มจะเป็นลูกค้า</span><span class="sxs-lookup"><span data-stu-id="99d5d-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="99d5d-170">ประวัติ InMail</span><span class="sxs-lookup"><span data-stu-id="99d5d-170">InMail history</span></span>

<span data-ttu-id="99d5d-171">ประวัติ LinkedIn InMail พร้อมใช้งานกับการเข้าถึงระดับสัญญาที่มีผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="99d5d-172">เมื่อมีการเปิดใช้งาน คุณสามารถดูประวัติ InMail ทั้งหมดได้พร้อมกับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="99d5d-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="99d5d-173">นอกจากนี้ คุณยังสามารถดูว่าใครอีกที่มาจากองค์กรของคุณที่ได้แลกเปลี่ยน InMail กับผู้สมัคร อย่างไรก็ตาม คุณไม่สามารถดูข้อความระหว่างพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="99d5d-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="99d5d-174">เพื่อดูประวัติ InMail ไปยังโปรไฟล์ของผู้สมัคร ไปที่แท็บ **LinkedIn** และเลื่อนไปยังด้านล่างของหน้าเพื่อดูประวัติ</span><span class="sxs-lookup"><span data-stu-id="99d5d-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="99d5d-175">คุณสามารถดูประวัติ InMail ได้ ถ้าคุณได้มีการสนทนากับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="99d5d-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="99d5d-176">ข้อความจาก InMail จะทำให้ตรงกันกับ Attract ทุกๆ สองชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="99d5d-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="99d5d-177">ประวัติบันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="99d5d-177">Notes history</span></span> 

<span data-ttu-id="99d5d-178">ประวัติบันทึกย่อของ LinkedIn จะพร้อมใช้งาน โดยมีการเข้าถึงระดับสัญญากับผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="99d5d-179">เมื่อเปิดใช้งาน คุณสามารถดูบันทึกย่อที่มีการรวบรวมเกี่ยวกับผู้สมัคร โดยผู้สรรหาที่แตกต่างกันจากองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="99d5d-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="99d5d-180">เมื่อต้องการดูประวัติบันทึกย่อ ไปที่โพรไฟล์ของผู้สมัคร ไปยังแท็บ **LinkedIn** และเลื่อนไปที่ด้านล่างของหน้าเพื่อดูประวัติ</span><span class="sxs-lookup"><span data-stu-id="99d5d-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="99d5d-181">คุณสามารถดูบันทึกย่อทั้งหมดเกี่ยวกับผู้สมัครจากผู้สรรหา LinkedIn ได้</span><span class="sxs-lookup"><span data-stu-id="99d5d-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="99d5d-182">โปรไฟล์ส่วนที่เหลือของ InMail</span><span class="sxs-lookup"><span data-stu-id="99d5d-182">InMail stub profile</span></span>

<span data-ttu-id="99d5d-183">โปรไฟล์ส่วนที่เหลือของ InMail พร้อมใช้งานกับการเข้าถึงระดับสัญญาที่มีผู้สรรหา LinkedIn</span><span class="sxs-lookup"><span data-stu-id="99d5d-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="99d5d-184">ถ้าผู้สมัครตกลงที่จะใช้โพรไฟล์ LinkedIn ร่วมกับผู้ใช้ทุกคนในองค์กรของคุณ คุณสามารถติดตามผู้สมัครได้ใน Attract และเรกคอร์ดผู้สมัครใหม่จะถูกสร้างขึ้นสำหรับผู้สมัครแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="99d5d-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="99d5d-185">คุณสามารถดูที่อยู่อีเมลของผู้สมัคร ถ้ามีผู้สมัครอยู่แล้วในระบบซึ่งมีที่อยู่อีเมล หรือได้เลือกที่แบ่งปันอยู่กับที่ผู้สรรหา</span><span class="sxs-lookup"><span data-stu-id="99d5d-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="99d5d-186">เมื่อต้องการดูรายการของผู้สมัคร ไปยัง **กลุ่ม Talent** เพื่อดูกลุ่ม talent ของ LinkedIn ที่สร้างระบบ</span><span class="sxs-lookup"><span data-stu-id="99d5d-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="99d5d-187">กลุ่ม talent นี้ประกอบด้วยรายชื่อผู้สมัครและโพรไฟล์ต้นขั้วของพวกเขา ตามที่ได้รับจาก LinkedIn ซึ่งแสดงชื่อและนามสกุลของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="99d5d-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="99d5d-188">รหัสอีเมลของผู้สมัครจะแสดงขึ้น ถ้ามีการเลือกผู้สมัครเพื่อแบ่งปันที่อยู่อีเมลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="99d5d-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
