---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 for Talent (11 มิถุนายน 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a1413ea43e852c78ede227b69c0f49c07944a872
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741638"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a><span data-ttu-id="b7ef5-103">มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Dynamics 365 for Talent (11 มิถุนายน 2019)</span><span class="sxs-lookup"><span data-stu-id="b7ef5-103">What's new or changed in Dynamics 365 for Talent (June 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7ef5-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="b7ef5-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="b7ef5-105">การเปลี่ยนแปลงใน Attract</span><span class="sxs-lookup"><span data-stu-id="b7ef5-105">Changes in Attract</span></span>

### <a name="search-engine-optimization-for-job-posts"></a><span data-ttu-id="b7ef5-106">การเพิ่มประสิทธิภาพโปรแกรมค้นหาสำหรับโพสต์งาน</span><span class="sxs-lookup"><span data-stu-id="b7ef5-106">Search engine optimization for job posts</span></span>

<span data-ttu-id="b7ef5-107">หลังจากที่คุณเปิดใช้งาน **การเพิ่มประสิทธิภาพโปรแกรมค้นหา** ใน Dynamics 365 for Talent: ศูนย์ผู้ดูแลระบบ Attract Attract แจ้ง Application Programming Interface (API) ในการจัดทำดัชนีของ Google เพื่อรวบรวมเว็บเพจ เมื่อใดก็ตามที่คุณเรียกใช้และโพสต์งานใหม่ หรือปรับปรุงงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b7ef5-107">After you turn on **Search Engine Optimization** in the Dynamics 365 for Talent: Attract Admin center, Attract informs the Google Indexing application programming interface (API) to crawl the webpage whenever you activate and post a new job or update an existing job.</span></span> <span data-ttu-id="b7ef5-108">ด้วยวิธีนี้ งานจะปรากฏขึ้นในผลลัพธ์การค้นหาสำหรับ Google และเครื่องมือค้นหาอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b7ef5-108">In this way, the job will appear in the search results for Google and other search engines.</span></span>

<span data-ttu-id="b7ef5-109">ในทำนองเดียวกัน เมื่อใดก็ตามที่คุณยกเลิกการโพสต์งาน Attract จะแจ้ง API ที่จัดทำดัชนี เพื่อให้งานที่ยกเลิกการโพสต์จะหยุดแสดงอยู่ในผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="b7ef5-109">Likewise, whenever you unpost a job, Attract informs the Indexing API, so that the unposted job will stop appearing in search results.</span></span>

> [!NOTE]
> <span data-ttu-id="b7ef5-110">ตัวรวบรวมเว็บไม่มีกรอบเวลาที่กำหนดไว้สำหรับการรวบรวมเว็บเพจหรือการปรับปรุงผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="b7ef5-110">Web crawlers don't have a defined timeframe for crawling webpages or updating search results.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="b7ef5-111">เร็วๆ นี้ใน Attract</span><span class="sxs-lookup"><span data-stu-id="b7ef5-111">Coming soon in Attract</span></span>

### <a name="job-approvals-appear-on-the-home-page"></a><span data-ttu-id="b7ef5-112">การอนุมัติงานปรากฏในโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="b7ef5-112">Job approvals appear on the home page</span></span>

<span data-ttu-id="b7ef5-113">การอนุมัติจะปรากฏในส่วน **การอนุมัติ** บนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="b7ef5-113">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="b7ef5-114">ผู้อนุมัติสามารถตรวจทานการอนุมัติของตนภายใต้ **กำหนดให้กับคุณ** ซึ่งแสดงรหัสงาน หัวข้องาน ผู้อนุมัติอื่นๆ และวันที่ที่กำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="b7ef5-114">Approvers can review their approvals under **Assigned to you**, which shows the job ID, the job title, other approvers, and the date when the job was assigned.</span></span> <span data-ttu-id="b7ef5-115">ผู้ใช้ที่ส่งงานให้กับการอนุมัติสามารถตรวจทานงานของตนได้ภายใต้ **ร้องขอโดยคุณ** ซึ่งแสดงผู้อนุมัติซึ่งยังคงต้องอนุมัติงานที่ส่ง</span><span class="sxs-lookup"><span data-stu-id="b7ef5-115">Users who submit a job for approval can review their jobs under **Requested by you**, which shows the approvers who must still approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="b7ef5-116">การเปลี่ยนแปลงในการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="b7ef5-116">Changes in Onboard</span></span>

<span data-ttu-id="b7ef5-117">รุ่นนี้มีการแก้ไขบักรองสำหรับ Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="b7ef5-117">This release includes minor bug fixes for Dynamics 365 for Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="b7ef5-118">การเปลี่ยนแปลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="b7ef5-118">Changes in Core HR</span></span>

<span data-ttu-id="b7ef5-119">การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้จะนำไปใช้กับการสร้างหมายเลข 8.1.2337</span><span class="sxs-lookup"><span data-stu-id="b7ef5-119">The changes that are described in this section apply to build number 8.1.2337.</span></span>

### <a name="platform-update-27"></a><span data-ttu-id="b7ef5-120">แพลตฟอร์ม update 27</span><span class="sxs-lookup"><span data-stu-id="b7ef5-120">Platform update 27</span></span>

<span data-ttu-id="b7ef5-121">สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการปรับปรุงแพลตฟอร์ม 27 ดูที่ [คุณลักษณะการแสดงตัวอย่างใน Dynamics 365 for Finance and Operations การปรับปรุงแพลตฟอร์ม 27 (มิถุนายน 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27)</span><span class="sxs-lookup"><span data-stu-id="b7ef5-121">For more details about Platform update 27, see [Preview features in Dynamics 365 for Finance and Operations platform update 27 (June 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span></span>

### <a name="feature-management-workspace-in-talent"></a><span data-ttu-id="b7ef5-122">พื้นที่ทำงานในการจัดการคุณลักษณะใน Talent</span><span class="sxs-lookup"><span data-stu-id="b7ef5-122">Feature management workspace in Talent</span></span>

<span data-ttu-id="b7ef5-123">พื้นที่ทำงาน **การจัดการคุณลักษณะ** ใน **การจัดการระบบ** ช่วยให้คุณสามารถดู เปิดใช้งาน ปิดใช้งาน และจัดกำหนดการคุณลักษณะ ที่ได้รับการจัดส่งในแต่ละรุ่น</span><span class="sxs-lookup"><span data-stu-id="b7ef5-123">The **Feature management** workspace in **System administration** lets you view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="b7ef5-124">ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด</span><span class="sxs-lookup"><span data-stu-id="b7ef5-124">By default, new features are turned off.</span></span> <span data-ttu-id="b7ef5-125">คุณสามารถใช้พื้นที่ทำงาน **การจัดการคุณลักษณะ** เพื่อเปิดใช้ และดูเอกสารประกอบได้</span><span class="sxs-lookup"><span data-stu-id="b7ef5-125">You can use the **Feature management** workspace to turn them on and view the documentation for them.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="b7ef5-126">การสนับสนุนเอนทิตี Common Data Service สำหรับฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b7ef5-126">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="b7ef5-127">ขณะนี้เอนทิตีของหน่วยงานที่ออกเอกสารให้การสนับสนุนฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b7ef5-127">The Issuing agency entity now supports custom fields.</span></span>

### <a name="new-common-data-service-entities"></a><span data-ttu-id="b7ef5-128">เอนทิตี Common Data Service ใหม่</span><span class="sxs-lookup"><span data-stu-id="b7ef5-128">New Common Data Service entities</span></span>

<span data-ttu-id="b7ef5-129">มีการเพิ่มเอนทิตีกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="b7ef5-129">The Task group entity has been added.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b7ef5-130">ในการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b7ef5-130">In preview</span></span>

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a><span data-ttu-id="b7ef5-131">คุณลักษณะการแสดงตัวอย่างจะเปิดใช้งานเฉพาะในสภาพแวดล้อม sandbox เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b7ef5-131">Preview features will be enabled only in sandbox environments</span></span>

<span data-ttu-id="b7ef5-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเผยแพร่การเปลี่ยนแปลง โปรดดู [เตรียมใช้งาน Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="b7ef5-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="b7ef5-133">เมื่อคุณจัดเตรียมอินสแตนท์ใหม่ของ Talent คุณสามารถบ่งชี้ว่าชนิดของอินสแตนซ์เป็นการผลิต หรือ Sandbox</span><span class="sxs-lookup"><span data-stu-id="b7ef5-133">When you provision a new instance of Talent, you can indicate whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="b7ef5-134">ชนิดของอินสแตนซ์ Sandbox อนุญาตให้มีการทดสอบของคุณลักษณะใหม่ก่อนเวลา</span><span class="sxs-lookup"><span data-stu-id="b7ef5-134">The Sandbox instance type allows for early testing of new features.</span></span> <span data-ttu-id="b7ef5-135">อินสแตนซ์ Talent ที่มีอยู่ทั้งหมดจะได้รับการปรับปรุงเป็นชนิดอินสแตนซ์ **การผลิต**</span><span class="sxs-lookup"><span data-stu-id="b7ef5-135">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="b7ef5-136">ถ้าคุณต้องการให้หนึ่งในอินสแตนซ์ที่มีอยู่ของคุณได้รับการปรับปรุงเป็นชนิดของอินสแตนซ์ **Sandbox** ติดต่อ [ฝ่ายสนับสนุน](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) เพื่อเริ่มต้นการร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="b7ef5-136">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="b7ef5-137">จำกัดชนิดการลางานในการร้องขอเวลาหยุดพัก</span><span class="sxs-lookup"><span data-stu-id="b7ef5-137">Restrict the leave types in time-off requests</span></span>

<span data-ttu-id="b7ef5-138">องค์กรสามารถให้ชนิดของการลางานหลายชนิดแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="b7ef5-138">Organizations can offer many types of leave to employees.</span></span> <span data-ttu-id="b7ef5-139">อย่างไรก็ตาม อาจไม่เหมาะสมสำหรับพนักงานที่จะส่งการร้องขอเวลาหยุดพักสำหรับชนิดการลางานบางชนิด</span><span class="sxs-lookup"><span data-stu-id="b7ef5-139">However, it might not be appropriate for employees to submit time-off requests for some leave types.</span></span> <span data-ttu-id="b7ef5-140">ชนิดการลางานเหล่านั้นอาจถูกจัดการโดยฝ่ายทรัพยากรบุคคล (HR) แทน</span><span class="sxs-lookup"><span data-stu-id="b7ef5-140">Those leave types might be managed by Human resources (HR) instead.</span></span> <span data-ttu-id="b7ef5-141">ในการนำออกใช้นี้ คุณสามารถตั้งค่าคอนฟิกได้ว่าชนิดของการลางานใดที่พนักงานสามารถส่งการร้องขอเวลาหยุดพักได้</span><span class="sxs-lookup"><span data-stu-id="b7ef5-141">In this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

## <a name="coming-soon-in-core-hr"></a><span data-ttu-id="b7ef5-142">เร็วๆ นี้ใน Core HR</span><span class="sxs-lookup"><span data-stu-id="b7ef5-142">Coming soon in Core HR</span></span>

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a><span data-ttu-id="b7ef5-143">ดูข้อมูลที่ขยายเกี่ยวกับประสิทธิภาพรายงานในการบริการตนเองของผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="b7ef5-143">View extended information about report performance in manager self-service</span></span>

<span data-ttu-id="b7ef5-144">ตัวเลือกใหม่จะช่วยให้ผู้จัดการสามารถดูประสิทธิภาพของทั้งรายงานโดยตรงและรายงานที่ขยายของตนได้</span><span class="sxs-lookup"><span data-stu-id="b7ef5-144">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="b7ef5-145">ในปัจจุบัน ผู้จัดการรายการสามารถกำหนดและปรับปรุงเป้าหมายผลการปฏิบัติงานและออกการตรวจทานใหม่</span><span class="sxs-lookup"><span data-stu-id="b7ef5-145">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="b7ef5-146">นอกจากนี้ ผู้จัดการโดยตรงและพนักงานของพวกเขาสามารถรักษาและปรับปรุงสมุดรายวันประสิทธิภาพ เพื่อช่วยรับประกันว่ากระบวนการตรวจทานประสิทธิภาพจะทำงานได้อย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="b7ef5-146">In addition, direct managers and their employees can maintain and update performance journals to help guarantee that the performance review process goes smoothly.</span></span> <span data-ttu-id="b7ef5-147">เมื่อมีการใช้การเปลี่ยนแปลงนี้ ผู้จัดการจะสามารถดูและรักษาข้อมูลที่เกี่ยวข้องกับประสิทธิภาพสำหรับรายงานแบบขยายของพวกเขา นอกเหนือจากรายงานโดยตรงของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b7ef5-147">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="b7ef5-148">พิมพ์การตรวจทานประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="b7ef5-148">Print performance reviews</span></span>

<span data-ttu-id="b7ef5-149">พนักงาน ผู้จัดการ และ HR จะสามารถพิมพ์การตรวจทานประสิทธิภาพของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="b7ef5-149">Employees, managers, and HR will be able to print an employee's performance review.</span></span>
