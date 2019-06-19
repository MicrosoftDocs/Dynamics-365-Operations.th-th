---
title: ลงประกาศงานลงในไซต์การทำงานภายนอกจาก Attract
description: หัวข้อนี้อธิบายวิธีการใช้ Dynamics 365 for Talent - Attract เพื่อลงประกาศงานไปยังไซต์การสรรหาบุคลากรภายนอก
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590493"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="a3786-103">ลงประกาศงานลงในไซต์การทำงานภายนอกจาก Attract</span><span class="sxs-lookup"><span data-stu-id="a3786-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3786-104">คุณต้องการเรียกดูตำแหน่งที่เปิดของคุณ ข้างหน้าผู้สมัครที่มีคุณสมบัติหลายรายที่สุดที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="a3786-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="a3786-105">ไซต์การสรรหาบุคลากร เช่น Broadbean ช่วยให้คุณบรรลุถึงเป้าหมายนี้</span><span class="sxs-lookup"><span data-stu-id="a3786-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="a3786-106">Microsoft Dynamics 365 talent: ขณะนี้ Attract ช่วยให้คุณลงประกาศงานไปยัง Broadbean และ Microsoft ให้ข้อเสนอใหม่ในพื้นที่นี้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="a3786-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="a3786-107">ลงประกาศงานไปยัง Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="a3786-108">ก่อนที่คุณจะสามารถลงประกาศงานไปยัง Broadbean คุณต้องตั้งค่าคอนฟิกการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="a3786-109">เพื่อลงประกาศงานไปยังไซต์ภายนอก คุณต้องมี [add-on การว่าจ้างที่ครอบคลุม](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)</span><span class="sxs-lookup"><span data-stu-id="a3786-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="a3786-110">เมื่อต้องการลงรายการบัญชีงานไปยัง Broadbean ผ่าน Attract คุณต้องมีการสมัครใช้งาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="a3786-111">คุณลักษณะนี้อยู่ในการแสดงตัวอย่างในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="a3786-111">This feature is currently in preview.</span></span> <span data-ttu-id="a3786-112">ถ้าคุณต้องการลอง คุณต้อง [เปิดในการตั้งค่าการจัดการ Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)</span><span class="sxs-lookup"><span data-stu-id="a3786-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="a3786-113">ตั้งค่าคอนฟิกการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="a3786-114">ลงชื่อเข้าใช้ Attract เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a3786-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="a3786-115">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ในมุมขวาบนของหน้า และจากนั้น **ศูนย์การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="a3786-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="a3786-116">บนแท็บ **การตั้งค่ากระดานงาน** ในส่วน **เปิดใช้งานการรวม Broadbean** เปิดการรวม</span><span class="sxs-lookup"><span data-stu-id="a3786-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="a3786-117">ติดต่อ Broadbean และป้อนข้อมูลของคุณใน **ชื่อผู้ใช้ รหัสไคลเอนต์ โทเคนการเข้ารหัส**</span><span class="sxs-lookup"><span data-stu-id="a3786-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="a3786-118">ข้อมูลประจำตัว Broadbean ของคุณมีความสำคัญ และเป็นความลับ</span><span class="sxs-lookup"><span data-stu-id="a3786-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="a3786-119">ดังนั้น จึงจัดเก็บ และแบ่งปันอย่างรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="a3786-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="a3786-120">ผู้ที่มีบทบาทผู้ดูแลระบบใน Attract สามารถดูข้อมูลประจำตัวเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="a3786-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="a3786-121">Microsoft และ Attract จะไม่เกี่ยวข้องในการสร้างและการรักษาค่าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a3786-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="a3786-122">เป็นความรับผิดชอบของคุณในการทำให้เป็นปัจจุบันใน Attract และในการทำงานกับ Broadbean เพื่อแก้ไขปัญหาใดๆ ที่เกี่ยวข้องกับข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="a3786-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="a3786-123">ลงประกาศงานไปยัง Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-123">Post a job to Broadbean</span></span>

<span data-ttu-id="a3786-124">หลังจากที่มีการเปิด Broadbean ผู้สรรหาและผู้ดูแลระบบสามารถลงประกาศงานได้</span><span class="sxs-lookup"><span data-stu-id="a3786-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="a3786-125">คุณต้องมีการใช้ URL สำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="a3786-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="a3786-126">ใน Attract เปิดงานที่คุณต้องการลงประกาศงานไปยัง Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="a3786-127">ในส่วน **การลงประกาศ** เลือกปุ่ม **ลงประกาศตอนนี้** ที่สอดคล้องกับ Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="a3786-128">ทำตามคำแนะนำในหน้าต่าง Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="a3786-129">Attract ส่งผ่านข้อมูลต่อไปนี้ไปยัง Broadbean:</span><span class="sxs-lookup"><span data-stu-id="a3786-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="a3786-130">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="a3786-130">Request ID</span></span>
- <span data-ttu-id="a3786-131">ตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="a3786-131">Job title</span></span>
- <span data-ttu-id="a3786-132">คำอธิบายงาน</span><span class="sxs-lookup"><span data-stu-id="a3786-132">Job description</span></span>
- <span data-ttu-id="a3786-133">สถานที่ตั้งของงาน</span><span class="sxs-lookup"><span data-stu-id="a3786-133">Job location</span></span>
- <span data-ttu-id="a3786-134">นำ URL ไปใช้</span><span class="sxs-lookup"><span data-stu-id="a3786-134">Apply URL</span></span>
- <span data-ttu-id="a3786-135">ข้อมูลผู้สรรหา</span><span class="sxs-lookup"><span data-stu-id="a3786-135">Recruiter information</span></span>

<span data-ttu-id="a3786-136">หลังจาก Broadbean ลงประกาศเสร็จสมบูรณ์ ส่วน **การลงประกาศ** ของงานใน Attract แสดงสถานะ Broadbean เป็น **ลงประกาศแล้ว**</span><span class="sxs-lookup"><span data-stu-id="a3786-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a3786-137">Broadbean ต้องการฟิลด์ **อุตสาหกรรม**</span><span class="sxs-lookup"><span data-stu-id="a3786-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="a3786-138">ในขณะนี้ ฟิลด์นี้ถูกตั้งค่าเป็น **IT** ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a3786-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="a3786-139">อย่างไรก็ตาม คุณสามารถเปลี่ยนค่าเป็นอุตสาหกรรมที่ถูกต้องในหน้าต่างสำหรับการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="a3786-140">ใช้เวลานานสำหรับ Broadbean ที่จะเสร็จสิ้นการลงประกาศงานของคุณไปยังบอร์ดงานทั้งหมดที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="a3786-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="a3786-141">ดังนั้น จึงอาจมีความล่าช้าเล็กน้อย ก่อนที่ Attract จะให้การปรับปรุงสถานะสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="a3786-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="a3786-142">ดูการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-142">View a Broadbean job posting</span></span>

<span data-ttu-id="a3786-143">หลังจากที่คุณลงประกาศงานไปยัง Broadbean คุณสามารถดูได้จาก Attract</span><span class="sxs-lookup"><span data-stu-id="a3786-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="a3786-144">ใน Attract เปิดงานที่คุณต้องการดูใน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="a3786-145">ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="a3786-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="a3786-146">การลงประกาศงาน Broadbean ปรากฏขึ้นในหน้าต่างใหม่</span><span class="sxs-lookup"><span data-stu-id="a3786-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="a3786-147">ปรับปรุงการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="a3786-148">คุณสามารถปรับปรุงการลงประกาศงาน Broadbean ได้ในสองวิธี</span><span class="sxs-lookup"><span data-stu-id="a3786-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="a3786-149">ใน Attract เปิดงานที่คุณต้องการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a3786-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="a3786-150">ในส่วน **การลงประกาศ** เลือกปุ่ม **ปรับปรุงประกาศ** ที่สอดคล้องกับ Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="a3786-151">แก้ไขการลงประกาศในหน้าต่าง Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="a3786-152">หรือ</span><span class="sxs-lookup"><span data-stu-id="a3786-152">–or–</span></span>

1. <span data-ttu-id="a3786-153">ใน Attract เปิดงานที่คุณต้องการดูใน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="a3786-154">ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="a3786-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="a3786-155">ในหน้าต่าง Broadbean แก้ไขรายละเอียดงาน และจากนั้น ลงประกาศงานซ้ำ</span><span class="sxs-lookup"><span data-stu-id="a3786-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="a3786-156">รายละเอียดงานใน Attract จะไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a3786-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="a3786-157">ลบการลงประกาศงาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="a3786-158">คุณสามารถลบการลงประกาศงานจาก Broadbean ได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="a3786-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="a3786-159">ใน Attract เปิดงานที่คุณต้องการลบ</span><span class="sxs-lookup"><span data-stu-id="a3786-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="a3786-160">ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ลบประกาศ**</span><span class="sxs-lookup"><span data-stu-id="a3786-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="a3786-161">หลังจากที่ Broadbean ลบงาน รายการ Broadbean ใน Attract มีปุ่ม **ลงประกาศตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="a3786-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="a3786-162">การมีอยู่ของปุ่มนี้บ่งชี้ว่า งานถูกลบออก และสามารถลงประกาศได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a3786-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="a3786-163">แก้ไขปัญหาการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="a3786-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="a3786-164">ถ้าคุณมีปัญหาในการลงประกาศงานไปยัง Broadbean ลองขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a3786-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="a3786-165">ตรวจสอบว่าข้อมูลประจำตัวของ Broadbean ที่คุณป้อนใน Attract ใช้ได้และถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a3786-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="a3786-166">ถ้าข้อมูลประจำตัวใช้ได้และถูกต้อง ติดต่อ [ฝ่ายสนับสนุนของ Broadbean](https://www.broadbean.com/resources/support/)</span><span class="sxs-lookup"><span data-stu-id="a3786-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="a3786-167">ถ้าปัญหายังคงอยู่ ติดต่อ [ฝ่ายสนับสนุนของ Microsoft](./talent-support.md)</span><span class="sxs-lookup"><span data-stu-id="a3786-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
