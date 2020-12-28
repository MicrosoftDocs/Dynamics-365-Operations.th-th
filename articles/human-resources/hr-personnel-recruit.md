---
title: สรรหาผู้สมัครงาน
description: หัวข้อนี้จะแสดงวิธีการสรรหาผู้สมัครใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669193"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="b8b65-103">สรรหาผู้สมัครงาน</span><span class="sxs-lookup"><span data-stu-id="b8b65-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="b8b65-104">Dynamics 365 Human Resources ช่วยคุณในการจัดการคำขอสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="b8b65-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="b8b65-105">นอกจากนี้ยังช่วยให้คุณสามารถเปลี่ยนผู้สมัครงานเป็นพนักงานได้อย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="b8b65-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="b8b65-106">ถ้าองค์กรของคุณใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก กระบวนการสรรหาบุคลากรของคุณอาจประกอบด้วยขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b8b65-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="b8b65-107">ป้อนคำขอสรรหาบุคลากรของคุณในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b8b65-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="b8b65-108">รับการอ้างอิงของผู้สมัครในทรัพยากรบุคคลจากแอปพลิเคชันการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="b8b65-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="b8b65-109">ดำเนินการขั้นตอนการอนุมัติของผู้สมัครในทรัพยากรบุคคลให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b8b65-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="b8b65-110">ถ้าคุณไม่ได้ใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก คุณยังสามารถจัดการผู้สมัครในทรัพยากรบุคคลด้วยตนเองได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b8b65-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="b8b65-111">ถ้าคุณเป็นผู้ดูแลระบบหรือนักพัฒนาและต้องการรวมทรัพยากรบุคคลกับแอปพลิเคชันการสรรหาบุคลากรที่สาม โปรดดูที่ [ตั้งค่าคอนฟิกการรวม Common Data Service](hr-admin-integration-common-data-service.md) และ [ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="b8b65-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="b8b65-112">นอกจากนี้ คุณยังสามารถพบแอปการรวมการสรรหาบุคลากรใน [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b8b65-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="b8b65-113">ถ้าต้องการลองคุณลักษณะพรีวิวสำหรับการรวมกับฮับ LinkedIn Talent โปรดดูที่ [รวมกับฮับ LinkedIn Talent](hr-admin-integration-linkedin.md)</span><span class="sxs-lookup"><span data-stu-id="b8b65-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="b8b65-114">เปิดใช้งานคำขอสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="b8b65-114">Enable recruiting requests</span></span>

<span data-ttu-id="b8b65-115">ถ้าคุณต้องการส่งคำขอสรรหาบุคลากรในทรัพยากรบุคคล ก่อนอื่นคุณต้องเปิดใช้งานฟังก์ชันใน **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="b8b65-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="b8b65-116">ในพื้นที่ทำงาน **การจัดการบุคลากร** ให้เลือก **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="b8b65-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b8b65-117">ภายใต้ **ตั้งค่า** พารามิเตอร์ **ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="b8b65-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="b8b65-118">บนแท็บ **ทั่วไป** ภายใต้ **การสรรหาบุคลากร** ให้ตั้งค่า **เปิดใช้งานคำขอการสรรหาบุคลากร** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b8b65-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![เปิดใช้งานคำขอสรรหาบุคลากร](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="b8b65-120">เพิ่มสถานที่ร้องขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="b8b65-120">Add a recruiting request location</span></span>

<span data-ttu-id="b8b65-121">ถ้าองค์กรของคุณมีหลายสถานที่ คุณสามารถเพิ่มได้เพื่อให้ผู้ขอสามารถเลือกสถานที่ที่จะทำงานของการสรรหาใหม่</span><span class="sxs-lookup"><span data-stu-id="b8b65-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="b8b65-122">สถานที่จะถูกรวมอยู่ในการโพสต์งาน</span><span class="sxs-lookup"><span data-stu-id="b8b65-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="b8b65-123">ในแถบค้นหา ให้ป้อน **สถานที่ร้องขอการสรรหาบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="b8b65-124">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b8b65-124">Select **New**.</span></span>

3. <span data-ttu-id="b8b65-125">ในฟิลด์ **สถานที่ร้องขอการสรรหาบุคลากร** ให้ป้อนชื่อสถานที่</span><span class="sxs-lookup"><span data-stu-id="b8b65-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![เพิ่มสถานที่ร้องขอการสรรหาบุคลากร](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="b8b65-127">ใน **คำอธิบาย** ป้อนคำอธิบายสำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="b8b65-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="b8b65-128">ภายใต้ **สถานที่** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="b8b65-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="b8b65-129">ถ้า popout **ที่อยู่ใหม่** ปรากฏขึ้น ให้ป้อนที่อยู่สำหรับสถานที่</span><span class="sxs-lookup"><span data-stu-id="b8b65-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![ป้อนที่อยู่](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="b8b65-131">ภายใต้ **ข้อมูลผู้ติดต่อ** ให้ป้อนข้อมูลสำหรับผู้ติดต่อของสถานที่</span><span class="sxs-lookup"><span data-stu-id="b8b65-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="b8b65-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b8b65-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="b8b65-133">เพิ่มคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="b8b65-133">Add a recruiting request</span></span>

<span data-ttu-id="b8b65-134">ผู้จัดการสามารถส่งคำขอการสรรหาบุคลากรในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b8b65-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="b8b65-135">ถ้าคุณใช้แอปพลิเคชันการสรรหาบุคลากรที่แยกต่างหาก การทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์จะส่งคำขอการสรรหาบุคลากรและเริ่มต้นกระบวนการสรรหาบุคลากรในแอปพลิเคชันดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b8b65-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="b8b65-136">หรือให้ทำกระบวนงานนี้ให้เสร็จสมบูรณ์เพื่อเริ่มต้นลำดับงานสำหรับกระบวนการสรรหาบุคลากรภายในของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="b8b65-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="b8b65-137">เลือก **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="b8b65-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="b8b65-138">เลือกแท็บ **ทีมงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="b8b65-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="b8b65-139">เลือก **คำขอเพื่อสรรหา**</span><span class="sxs-lookup"><span data-stu-id="b8b65-139">Select  **Request to recruit**.</span></span>

   ![เริ่มต้นคำขอการสรรหาบุคลากร](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="b8b65-141">กรอกข้อมูลในฟิลด์ **คำอธิบาย** **งาน** และ **วันที่เริ่มต้นโดยประมาณ**</span><span class="sxs-lookup"><span data-stu-id="b8b65-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![ดำเนินการคำขอสรรหาบุคลากรให้เสร็จสมบูรณ์](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="b8b65-143">เลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="b8b65-143">Select **Continue**.</span></span> <span data-ttu-id="b8b65-144">คำขอการสรรหาบุคลากรสำหรับตำแหน่งของคุณจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b8b65-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="b8b65-145">ภายใต้ **ทั่วไป** ให้เลือกผู้สรรหาจากเมนูแบบหล่นลง **ผู้สรรหา** และจากนั้น เลือกสถานที่จากเมนูแบบหล่นลง **สถานที่ร้องขอการสรรหาบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="b8b65-146">ภายใต้ **งาน** ให้เปลี่ยนข้อมูลใดๆ ตามความจำเป็น แล้วจากนั้น เลือก **สร้างรายละเอียดจากงาน**</span><span class="sxs-lookup"><span data-stu-id="b8b65-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![สร้างรายละเอียดจากงาน](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="b8b65-148">ส่วนที่เหลือของคำขอการสรรหาบุคลากรจะเติมด้วยข้อมูลเริ่มต้นสำหรับงานที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="b8b65-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="b8b65-149">ภายใต้ **คำอธิบายภายนอก** ให้ป้อนคำอธิบายงานที่เชื่อมต่อกับภายนอก</span><span class="sxs-lookup"><span data-stu-id="b8b65-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="b8b65-150">ภายใต้ **ตำแหน่ง** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกตำแหน่งสำหรับคำขอการสรรหาบุคลากรนี้</span><span class="sxs-lookup"><span data-stu-id="b8b65-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![เพิ่มตำแหน่งงาน](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="b8b65-152">ภายใต้ **ทักษะ** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกทักษะ</span><span class="sxs-lookup"><span data-stu-id="b8b65-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="b8b65-153">ภายใต้ **ข้อกำหนดด้านการศึกษา** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกค่าจากเมนูแบบหล่นลง **การศึกษา** และ **ระดับของการศึกษา**</span><span class="sxs-lookup"><span data-stu-id="b8b65-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![เพิ่มข้อกำหนดด้านการศึกษา](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="b8b65-155">ภายใต้ **ข้อคิดเห็น** ให้เพิ่มข้อคิดเห็นตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b8b65-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="b8b65-156">ภายใต้ **ค่าตอบแทน** เลือกระดับจากเมนูแบบหล่นลง **ระดับ** แล้วจากนั้น ปรับ **ขีดจำกัดต่ำสุด** **จุดควบคุม** และ **ขีดจำกัดสูงสุด** ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b8b65-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="b8b65-157">เมื่อคำขอการสรรหาบุคลากรของคุณเสร็จสมบูรณ์แล้ว และคุณพร้อมที่จะเริ่มกระบวนการสรรหาบุคลากร ให้เลือก **เรียกใช้งาน** ในแถบเมนู</span><span class="sxs-lookup"><span data-stu-id="b8b65-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![เรียกใช้คำขอการสรรหาบุคลากร](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="b8b65-159">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b8b65-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="b8b65-160">ดูและแก้ไขคำขอการสรรหาบุคลากรของคุณ</span><span class="sxs-lookup"><span data-stu-id="b8b65-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="b8b65-161">ถ้าคุณเป็นผู้จัดการและต้องการดูคำขอของคุณเอง:</span><span class="sxs-lookup"><span data-stu-id="b8b65-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="b8b65-162">เลือก **ระบบบริการตนเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="b8b65-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="b8b65-163">เลือกแท็บ **ทีมงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="b8b65-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="b8b65-164">ภายใต้ **ข้อมูลทีมงานของฉัน** ให้เลือกแท็บ **คำขอการสรรหาบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![เลือกแท็บคำขอการสรรหาบุคลากร](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="b8b65-166">ถ้าต้องการดูหรือแก้ไขคำขอการสรรหาบุคลากร ให้เลือกในกริด</span><span class="sxs-lookup"><span data-stu-id="b8b65-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="b8b65-167">ถ้าคุณเป็นผู้เชี่ยวชาญด้าน HR หรือต้องการดูคำขอการสรรหาทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="b8b65-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="b8b65-168">เลือก **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="b8b65-169">เลือก **คำขอการสรรหาบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-169">Select **Recruiting requests**.</span></span>

   ![ดูคำขอการสรรหาบุคลากรในการจัดการบุคลากร](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="b8b65-171">ถ้าต้องการดูหรือแก้ไขคำขอการสรรหาบุคลากร ให้เลือกในกริด</span><span class="sxs-lookup"><span data-stu-id="b8b65-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="b8b65-172">เพิ่มหรือแก้ไขโพรไฟล์ผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b8b65-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="b8b65-173">ถ้าองค์กรของคุณได้รวมกับแอปพลิเคชันอื่นเพื่อจัดการคำขอการสรรหาบุคลากร คำขอการสรรหาบุคลากรจะถูกส่งต่อไปยังแอปพลิเคชันนั้น</span><span class="sxs-lookup"><span data-stu-id="b8b65-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="b8b65-174">แอปพลิเคชันการสรรหาบุคลากรส่งข้อมูลผู้สมัครกลับไปยังทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b8b65-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="b8b65-175">มิฉะนั้น คุณสามารถปฏิบัติตามกระบวนการสรรหาบุคลากรภายในของตนเอง และป้อนข้อมูลผู้สมัครด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b8b65-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="b8b65-176">เลือก **การจัดการบุคลากร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="b8b65-177">เลือก **ลิงก์**</span><span class="sxs-lookup"><span data-stu-id="b8b65-177">Select **Links**.</span></span>

3. <span data-ttu-id="b8b65-178">ภายใต้ **การสรรหาบุคลากร** ให้เลือก **ผู้สมัคร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![ดูผู้สมัคร](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="b8b65-180">เมื่อต้องการเพิ่มผู้สมัคร ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b8b65-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="b8b65-181">ถ้าต้องการแก้ไขผู้สมัครที่มีอยู่ ให้เลือกผู้สมัครจากรายการ และจากนั้นเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b8b65-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="b8b65-182">โพรไฟล์ผู้สมัครจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b8b65-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="b8b65-183">ภายใต้ **สรุปผู้สมัคร** ป้อนหรือแก้ไขข้อมูลผู้สมัครตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b8b65-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="b8b65-184">ภายใต้ **คำขอการสรรหาบุคลากร** ให้เลือกคำขอการสรรหาบุคลากรเพื่อลิงค์กับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b8b65-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="b8b65-185">จากนั้นให้ดำเนินการ **วันที่เริ่มต้นโดยประมาณ** **การว่าจ้างผู้จัดการ** **ตำแหน่ง** และ **ฟิลด์คำอธิบาย** ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="b8b65-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![ลิงค์กับคำขอการสรรหาบุคลากร](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="b8b65-187">กรอกข้อมูลทั้งหมดในพื้นที่ต่อไปนี้ที่คุณต้องการรวมไว้ในเรกคอร์ดของผู้สมัคร:</span><span class="sxs-lookup"><span data-stu-id="b8b65-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="b8b65-188">**ข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="b8b65-188">**Comments**</span></span>
   - <span data-ttu-id="b8b65-189">**ประสบการณ์การทำงาน**</span><span class="sxs-lookup"><span data-stu-id="b8b65-189">**Professional experience**</span></span>
   - <span data-ttu-id="b8b65-190">**ข้อมูลการติดต่อ**</span><span class="sxs-lookup"><span data-stu-id="b8b65-190">**Contact information**</span></span>
   - <span data-ttu-id="b8b65-191">**การศึกษา**</span><span class="sxs-lookup"><span data-stu-id="b8b65-191">**Education**</span></span>
   - <span data-ttu-id="b8b65-192">**ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="b8b65-192">**Skills**</span></span>
   - <span data-ttu-id="b8b65-193">**ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="b8b65-193">**Certificates**</span></span>
   - <span data-ttu-id="b8b65-194">**การคัดเลือก**</span><span class="sxs-lookup"><span data-stu-id="b8b65-194">**Screenings**</span></span>

8. <span data-ttu-id="b8b65-195">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b8b65-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="b8b65-196">จ้างงานผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b8b65-196">Hire a candidate</span></span>

<span data-ttu-id="b8b65-197">เมื่อคุณพร้อมที่จะจ้างงานผู้สมัคร ให้ทำตามกระบวนงานนี้เพื่อเปลี่ยนผู้สมัครเป็นพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b8b65-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="b8b65-198">บนฟอร์มผู้สมัคร ให้เลือก **จ้าง**</span><span class="sxs-lookup"><span data-stu-id="b8b65-198">On the candidate form, select **Hire**.</span></span>

   ![จ้างงานผู้สมัคร](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="b8b65-200">บนฟอร์ม **จ้างผู้ปฏิบัติงานใหม่** ภายใต้ **รายละเอียด** ให้กรอกข้อมูลในฟิลด์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b8b65-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![ป้อนรายละเอียดการจ้างงานใหม่](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="b8b65-202">ภายใต้ **รายละเอียดตำแหน่ง** ให้ตรวจสอบและเปลี่ยนข้อมูลตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b8b65-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="b8b65-203">ภายใต้ **รายการตรวจสอบการเตรียมความพร้อม** เลือกรายการตรวจสอบการเตรียมความพร้อมที่เกี่ยวข้องสำหรับพนักงานนี้</span><span class="sxs-lookup"><span data-stu-id="b8b65-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="b8b65-204">เลือก **ดำเนินการต่อ** เพื่อสร้างเรกคอร์ดพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b8b65-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="b8b65-205">โดยขึ้นอยู่กับลำดับงานขององค์กรของคุณ เรกคอร์ดผู้สมัครอาจมีขั้นตอนการอนุมัติเพิ่มเติม ก่อนที่จะกลายเป็นเรกคอร์ดพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b8b65-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="b8b65-206">ตัดสินใจที่จะไม่จ้างผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b8b65-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="b8b65-207">ถ้าคุณเลือกที่จะไม่จ้างผู้สมัคร ให้ทำตามกระบวนงานนี้เพื่อลบออกจากกระบวนการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="b8b65-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="b8b65-208">บนฟอร์มผู้สมัคร ให้เลือก **ไม่จ้าง**</span><span class="sxs-lookup"><span data-stu-id="b8b65-208">On the candidate form, select **Do not hire**.</span></span>

   ![ไม่จ้างงานผู้สมัคร](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="b8b65-210">เลือก **รหัสเหตุผล** และรวมข้อคิดเห็นใดๆ</span><span class="sxs-lookup"><span data-stu-id="b8b65-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="b8b65-211">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b8b65-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="b8b65-212">ยกเลิกผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="b8b65-212">Dismiss a candidate</span></span>

<span data-ttu-id="b8b65-213">ถ้าจำเป็น คุณสามารถยกเลิกผู้สมัครได้หลังจากจ้างงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="b8b65-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="b8b65-214">ตัวอย่างเช่น ผู้สมัครอาจปฏิเสธข้อเสนอของคุณ หรือไม่แสดงตัวในวันแรกของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b8b65-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="b8b65-215">บนฟอร์มผู้สมัคร ให้เลือก **ยกเลิกผู้สมัคร**</span><span class="sxs-lookup"><span data-stu-id="b8b65-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![ยกเลิกผู้สมัคร](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="b8b65-217">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b8b65-217">See also</span></span>

[<span data-ttu-id="b8b65-218">ตั้งค่าคอนฟิกเอนทิตีเสมือน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b8b65-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="b8b65-219">จัดระเบียบบุคลากรของคุณ</span><span class="sxs-lookup"><span data-stu-id="b8b65-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="b8b65-220">ตั้งค่าส่วนประกอบของงาน</span><span class="sxs-lookup"><span data-stu-id="b8b65-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)