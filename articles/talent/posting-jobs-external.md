---
title: ลงประกาศงานลงในไซต์การทำงานภายนอกจาก Attract
description: หัวข้อนี้อธิบายวิธีการใช้ Dynamics 365 for Talent - Attract เพื่อลงประกาศงานไปยังไซต์การสรรหาบุคลากรภายนอก
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519221"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="bda19-103">ลงประกาศงานลงในไซต์การทำงานภายนอกจาก Attract</span><span class="sxs-lookup"><span data-stu-id="bda19-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bda19-104">คุณต้องการเรียกดูตำแหน่งที่เปิดของคุณ ข้างหน้าผู้สมัครที่มีคุณสมบัติหลายรายที่สุดที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="bda19-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="bda19-105">ไซต์การสรรหาบุคลากร เช่น Broadbean ช่วยให้คุณบรรลุถึงเป้าหมายนี้</span><span class="sxs-lookup"><span data-stu-id="bda19-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="bda19-106">Microsoft Dynamics 365 talent: ขณะนี้ Attract ช่วยให้คุณลงประกาศงานไปยัง Broadbean และ Microsoft ให้ข้อเสนอใหม่ในพื้นที่นี้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="bda19-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="bda19-107">ลงประกาศงานไปยัง Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="bda19-108">ก่อนที่คุณจะสามารถลงประกาศงานไปยัง Broadbean คุณต้องตั้งค่าคอนฟิกการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="bda19-109">เพื่อลงประกาศงานไปยังไซต์ภายนอก คุณต้องมี [add-on การว่าจ้างที่ครอบคลุม](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)</span><span class="sxs-lookup"><span data-stu-id="bda19-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="bda19-110">คุณลักษณะนี้อยู่ในการแสดงตัวอย่างในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="bda19-110">This feature is currently in preview.</span></span> <span data-ttu-id="bda19-111">ถ้าคุณต้องการลอง คุณต้อง [เปิดในการตั้งค่าการจัดการ Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)</span><span class="sxs-lookup"><span data-stu-id="bda19-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="bda19-112">ตั้งค่าคอนฟิกการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="bda19-113">ลงชื่อเข้าใช้ Attract เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="bda19-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="bda19-114">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ในมุมขวาบนของหน้า และจากนั้น **ศูนย์การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="bda19-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="bda19-115">บนแท็บ **การตั้งค่ากระดานงาน** ในส่วน **เปิดใช้งานการรวม Broadbean** เปิดการรวม</span><span class="sxs-lookup"><span data-stu-id="bda19-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="bda19-116">ติดต่อ Broadbean และป้อนข้อมูลของคุณใน **ชื่อผู้ใช้ รหัสไคลเอนต์ โทเคนการเข้ารหัส**</span><span class="sxs-lookup"><span data-stu-id="bda19-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="bda19-117">ข้อมูลประจำตัว Broadbean ของคุณมีความสำคัญ และเป็นความลับ</span><span class="sxs-lookup"><span data-stu-id="bda19-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="bda19-118">ดังนั้น จึงจัดเก็บ และแบ่งปันอย่างรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="bda19-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="bda19-119">ผู้ที่มีบทบาทผู้ดูแลระบบใน Attract สามารถดูข้อมูลประจำตัวเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="bda19-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="bda19-120">Microsoft และ Attract จะไม่เกี่ยวข้องในการสร้างและการรักษาค่าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="bda19-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="bda19-121">เป็นความรับผิดชอบของคุณในการทำให้เป็นปัจจุบันใน Attract และในการทำงานกับ Broadbean เพื่อแก้ไขปัญหาใดๆ ที่เกี่ยวข้องกับข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="bda19-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="bda19-122">ลงประกาศงานไปยัง Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-122">Post a job to Broadbean</span></span>

<span data-ttu-id="bda19-123">หลังจากที่มีการเปิด Broadbean ผู้สรรหาและผู้ดูแลระบบสามารถลงประกาศงานได้</span><span class="sxs-lookup"><span data-stu-id="bda19-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="bda19-124">คุณต้องมีการใช้ URL สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="bda19-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="bda19-125">ใน Attract เปิดงานที่คุณต้องการลงประกาศงานไปยัง Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="bda19-126">ในส่วน **การลงประกาศ** เลือกปุ่ม **ลงประกาศตอนนี้** ที่สอดคล้องกับ Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="bda19-127">ทำตามคำแนะนำในหน้าต่าง Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="bda19-128">Attract ส่งผ่านข้อมูลต่อไปนี้ไปยัง Broadbean:</span><span class="sxs-lookup"><span data-stu-id="bda19-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="bda19-129">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="bda19-129">Request ID</span></span>
- <span data-ttu-id="bda19-130">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="bda19-130">Job title</span></span>
- <span data-ttu-id="bda19-131">คำอธิบายงาน</span><span class="sxs-lookup"><span data-stu-id="bda19-131">Job description</span></span>
- <span data-ttu-id="bda19-132">สถานที่ตั้งของงาน</span><span class="sxs-lookup"><span data-stu-id="bda19-132">Job location</span></span>
- <span data-ttu-id="bda19-133">นำ URL ไปใช้</span><span class="sxs-lookup"><span data-stu-id="bda19-133">Apply URL</span></span>
- <span data-ttu-id="bda19-134">ข้อมูลผู้สรรหา</span><span class="sxs-lookup"><span data-stu-id="bda19-134">Recruiter information</span></span>

<span data-ttu-id="bda19-135">หลังจาก Broadbean ลงประกาศเสร็จสมบูรณ์ ส่วน **การลงประกาศ** ของงานใน Attract แสดงสถานะ Broadbean เป็น **ลงประกาศแล้ว**</span><span class="sxs-lookup"><span data-stu-id="bda19-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="bda19-136">Broadbean ต้องการฟิลด์ **อุตสาหกรรม**</span><span class="sxs-lookup"><span data-stu-id="bda19-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="bda19-137">ในขณะนี้ ฟิลด์นี้ถูกตั้งค่าเป็น **IT** ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bda19-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="bda19-138">อย่างไรก็ตาม คุณสามารถเปลี่ยนค่าเป็นอุตสาหกรรมที่ถูกต้องในหน้าต่างสำหรับการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="bda19-139">ใช้เวลานานสำหรับ Broadbean ที่จะเสร็จสิ้นการลงประกาศงานของคุณไปยังบอร์ดงานทั้งหมดที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="bda19-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="bda19-140">ดังนั้น จึงอาจมีความล่าช้าเล็กน้อย ก่อนที่ Attract จะให้การปรับปรุงสถานะสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="bda19-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="bda19-141">ดูการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-141">View a Broadbean job posting</span></span>

<span data-ttu-id="bda19-142">หลังจากที่คุณลงประกาศงานไปยัง Broadbean คุณสามารถดูได้จาก Attract</span><span class="sxs-lookup"><span data-stu-id="bda19-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="bda19-143">ใน Attract เปิดงานที่คุณต้องการดูใน Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="bda19-144">ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="bda19-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="bda19-145">การลงประกาศงาน Broadbean ปรากฏขึ้นในหน้าต่างใหม่</span><span class="sxs-lookup"><span data-stu-id="bda19-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="bda19-146">ปรับปรุงการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="bda19-147">คุณสามารถปรับปรุงการลงประกาศงาน Broadbean ได้ในสองวิธี</span><span class="sxs-lookup"><span data-stu-id="bda19-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="bda19-148">ใน Attract เปิดงานที่คุณต้องการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="bda19-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="bda19-149">ในส่วน **การลงประกาศ** เลือกปุ่ม **ปรับปรุงประกาศ** ที่สอดคล้องกับ Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="bda19-150">แก้ไขการลงประกาศในหน้าต่าง Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="bda19-151">หรือ</span><span class="sxs-lookup"><span data-stu-id="bda19-151">–or–</span></span>

1. <span data-ttu-id="bda19-152">ใน Attract เปิดงานที่คุณต้องการดูใน Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="bda19-153">ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="bda19-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="bda19-154">ในหน้าต่าง Broadbean แก้ไขรายละเอียดงาน และจากนั้น ลงประกาศงานซ้ำ</span><span class="sxs-lookup"><span data-stu-id="bda19-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="bda19-155">รายละเอียดงานใน Attract จะไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="bda19-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="bda19-156">ลบการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="bda19-157">คุณสามารถลบการลงประกาศงานจาก Broadbean ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="bda19-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="bda19-158">ใน Attract เปิดงานที่คุณต้องการลบ</span><span class="sxs-lookup"><span data-stu-id="bda19-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="bda19-159">ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ลบประกาศ**</span><span class="sxs-lookup"><span data-stu-id="bda19-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="bda19-160">หลังจากที่ Broadbean ลบงาน รายการ Broadbean ใน Attract มีปุ่ม **ลงประกาศตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="bda19-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="bda19-161">การมีอยู่ของปุ่มนี้บ่งชี้ว่า งานถูกลบออก และสามารถลงประกาศได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="bda19-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="bda19-162">แก้ไขปัญหาการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="bda19-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="bda19-163">ถ้าคุณมีปัญหาในการลงประกาศงานไปยัง Broadbean ลองขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="bda19-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="bda19-164">ตรวจสอบว่าข้อมูลประจำตัวของ Broadbean ที่คุณป้อนใน Attract ใช้ได้และถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="bda19-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="bda19-165">ถ้าข้อมูลประจำตัวใช้ได้และถูกต้อง ติดต่อ [ฝ่ายสนับสนุนของ Broadbean](https://www.broadbean.com/resources/support/)</span><span class="sxs-lookup"><span data-stu-id="bda19-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="bda19-166">ถ้าปัญหายังคงอยู่ ติดต่อ [ฝ่ายสนับสนุนของ Microsoft](./talent-support.md)</span><span class="sxs-lookup"><span data-stu-id="bda19-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
