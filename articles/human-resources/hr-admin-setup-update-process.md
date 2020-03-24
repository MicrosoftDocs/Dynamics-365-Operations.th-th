---
title: อัปเดตกระบวนการ
description: Microsoft Dynamics 365 Human Resources เป็นซอฟต์แวร์จริงในฐานะบริการ (SaaS) ที่ให้การอัปเดตของการบริการระยะไกลที่ต่อเนื่องสำหรับแอพลิเคชันและการเปลี่ยนแปลงแพลตฟอร์ม
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092212"
---
# <a name="update-process"></a><span data-ttu-id="6c5ed-103">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-103">Update process</span></span>

<span data-ttu-id="6c5ed-104">Microsoft Dynamics 365 Human Resources เป็นซอฟต์แวร์จริงในฐานะบริการ (SaaS) ที่มีการอัปเดตของการบริการระยะไกลที่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="6c5ed-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="6c5ed-105">การอัปเดตเหล่านี้จะมีการเปลี่ยนแปลงทั้งโปรแกรมประยุกต์และแพลตฟอร์ม ซึ่งมักให้การปรับปรุงที่สำคัญแก่การบริการ รวมถึงการอัปเดตตามข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="6c5ed-106">นโยบายการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-106">Update policy</span></span>

<span data-ttu-id="6c5ed-107">การอัพเดตจะถูกนำออกใช้เป็นช่วงเวลาตามปกติกับสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6c5ed-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="6c5ed-108">ทรัพยากรบุคคลได้รับการสนับสนุนตาม [นโยบายของ Microsoft Lifecycle](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ซึ่งให้แนวทางปฏิบัติอย่างต่อเนื่อง และคาดการณ์ได้สำหรับความพร้อมในการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="6c5ed-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="6c5ed-109">ระยะความถี่การนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-109">Release cadence</span></span>

<span data-ttu-id="6c5ed-110">การอัพเดตทรัพยากรบุคคลจะใช้กับสภาพแวดล้อมทั้งหมดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="6c5ed-111">ทรัพยากรบุคคลมีการนำออกใช้สองชนิดดังนี้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="6c5ed-112">**การอัปเดตบริการ**: การอัปเดตรายสัปดาห์ที่รวมถึงการแก้ไขปัญหาบักและลักษณะการทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="6c5ed-112">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="6c5ed-113">การอัปเดตบริการมีการอัปเดตแพลตฟอร์มที่ใช้ได้เมื่อมีการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="6c5ed-114">เพื่อให้ได้แนวคิดเมื่อนำออกใช้การอัปเดตแพลตฟอร์ม ดูที่ [ตารางที่ 3: การนำออกใช้แพลตฟอร์ม](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="6c5ed-115">โดยปกติการอัปเดตรายสัปดาห์จะถูกนำออกใช้ในวันพุธ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-115">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="6c5ed-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดตรายสัปดาห์ ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-116">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="6c5ed-117">ศูนย์ข้อมูลที่ได้รับการสนับสนุนทั้งหมดมีการอัปเดตรายสัปดาห์ เว้นแต่จะมีการระบุไว้เป็นอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="6c5ed-117">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="6c5ed-118">โดยทั่วไป การอัปเดตรายสัปดาห์จะเริ่มต้นในวันพุธ และทำให้เสร็จสมบูรณ์ภายในวันอาทิตย์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-118">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="6c5ed-119">ภูมิภาคสหรัฐอเมริกา ออสเตรเลีย ยุโรป อังกฤษ เอเชียและแคนาดารวมอยู่ในการอัปเดตรายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-119">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="6c5ed-120">**การอัปเดตโซลูชัน Common Data Service**: การอัปเดตเหล่านี้เกิดขึ้นโดยประมาณทุก ๆ 6 สัปดาห์ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-120">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="6c5ed-121">ซึ่งรวมถึงเอนทิตีใหม่และการเปลี่ยนแปลงที่เกิดขึ้นกับเอนทิตีที่มีอยู่ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6c5ed-121">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="6c5ed-122">การอัปเดตเหล่านี้จะนำออกไปสู่ภูมิภาคเดียวกันกับการอัปเดตรายสัปดาห์ และใช้เวลาประมาณหกสัปดาห์ในการทำซ้ำโดยผ่านศูนย์ข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6c5ed-122">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="6c5ed-123">การอัปเดตโซลูชันอาจหรืออาจไม่สอดคล้องกับการอัปเดตการบริการรายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-123">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="6c5ed-124">ตารางต่อไปนี้แสดงกำหนดการตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6c5ed-124">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="6c5ed-125">สัปดาห์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-125">Week</span></span> | <span data-ttu-id="6c5ed-126">ชนิดการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-126">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="6c5ed-127">1</span><span class="sxs-lookup"><span data-stu-id="6c5ed-127">1</span></span> | <span data-ttu-id="6c5ed-128">การอัปเดตบริการ (ภูมิภาคทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-128">Service update (all regions)</span></span> |
| <span data-ttu-id="6c5ed-129">2</span><span class="sxs-lookup"><span data-stu-id="6c5ed-129">2</span></span> | <span data-ttu-id="6c5ed-130">การอัปเดตบริการ (ภูมิภาคทั้งหมด) + การอัปเดตโซลูชัน (สัปดาห์ 1 ภูมิภาค)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-130">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="6c5ed-131">3</span><span class="sxs-lookup"><span data-stu-id="6c5ed-131">3</span></span> | <span data-ttu-id="6c5ed-132">การอัปเดตบริการ (ภูมิภาคทั้งหมด) + การอัปเดตโซลูชัน (สัปดาห์ 2 ภูมิภาค)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-132">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="6c5ed-133">4</span><span class="sxs-lookup"><span data-stu-id="6c5ed-133">4</span></span> | <span data-ttu-id="6c5ed-134">การอัปเดตบริการ (ภูมิภาคทั้งหมด) + การอัปเดตโซลูชัน (สัปดาห์ 3 ภูมิภาค)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-134">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="6c5ed-135">5</span><span class="sxs-lookup"><span data-stu-id="6c5ed-135">5</span></span> | <span data-ttu-id="6c5ed-136">การอัปเดตบริการ (ภูมิภาคทั้งหมด) + การอัปเดตโซลูชัน (สัปดาห์ 4 ภูมิภาค)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-136">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="6c5ed-137">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="6c5ed-137">6</span></span> | <span data-ttu-id="6c5ed-138">การอัปเดตบริการ (ภูมิภาคทั้งหมด) + การอัปเดตโซลูชัน (สัปดาห์ 5 ภูมิภาค)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-138">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="6c5ed-139">7</span><span class="sxs-lookup"><span data-stu-id="6c5ed-139">7</span></span> | <span data-ttu-id="6c5ed-140">การอัปเดตบริการ (ภูมิภาคทั้งหมด) + การอัปเดตโซลูชัน (สัปดาห์ 6 ภูมิภาค)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-140">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="6c5ed-141">8</span><span class="sxs-lookup"><span data-stu-id="6c5ed-141">8</span></span> | <span data-ttu-id="6c5ed-142">การอัปเดตบริการ (ภูมิภาคทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-142">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="6c5ed-143">การอัปเดตโซลูชันมีอยู่ในศูนย์ข้อมูลทั้งหมดเมื่อมีการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-143">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="6c5ed-144">ถ้าคุณไม่ต้องการรอให้การอัปเดตจำลองแบบโดยอัตโนมัติ คุณสามารถใช้การอัปเดตใด ๆ เหล่านี้กับสภาพแวดล้อมใด ๆ ในศูนย์ข้อมูลใด ๆ ได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6c5ed-144">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="6c5ed-145">เมื่อต้องการ ทรัพยากรบุคคลจะมีชนิดการแก้ไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c5ed-145">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="6c5ed-146">**การแก้ไข (แก้ไขด่วน)**: แก้ไขบักที่อาจเกิดขึ้นทั้งกับหรือนอกเหนือจากการนำออกใช้การอัปเดตบริการรายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-146">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="6c5ed-147">**การแก้ไขกรณีฉุกเฉิน**: การแก้ไขด่วนอัตโนมัติและเชิงรับมีการทำงานในลักษณะที่เป็นแบบสแตนด์อโลน อาจรวมถึงการเปลี่ยนแปลงการตั้งค่าคอนฟิกอย่างเดียวหรือรหัสเพื่อแก้ปัญหาการใช้งานไซต์ที่ถ่ายทอดสด และอาจเกิดขึ้นนอกเหนือจากจากการนำออกใช้การอัปเดตบริการรายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-147">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="6c5ed-148">การนำออกใช้มีการตรวจสอบ ทดสอบและตรวจสอบความถูกต้องบนสภาพแวดล้อมภายใน</span><span class="sxs-lookup"><span data-stu-id="6c5ed-148">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="6c5ed-149">หลังจากที่มีการอนุมัติแล้วแล้ว การสร้างจะถูกนำไปใช้เพื่อการผลิต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-149">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="6c5ed-150">ข้อยกเว้นในปี 2019</span><span class="sxs-lookup"><span data-stu-id="6c5ed-150">Exceptions in 2019</span></span>

<span data-ttu-id="6c5ed-151">วันที่ต่อไปนี้จะมีข้อยกเว้นกำหนดการนำออกใช้ปกติ:</span><span class="sxs-lookup"><span data-stu-id="6c5ed-151">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="6c5ed-152">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="6c5ed-152">Date</span></span> | <span data-ttu-id="6c5ed-153">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6c5ed-153">Description</span></span> |
| --- | --- |
| <span data-ttu-id="6c5ed-154">สัปดาห์ของวันที่ 25 เดือนพฤศจิกายน</span><span class="sxs-lookup"><span data-stu-id="6c5ed-154">Week of November 25</span></span> | <span data-ttu-id="6c5ed-155">ไม่มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-155">No updates</span></span> |
| <span data-ttu-id="6c5ed-156">สัปดาห์ของวันที่ 16 เดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="6c5ed-156">Week of December 16</span></span> | <span data-ttu-id="6c5ed-157">การอัปเดตรองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6c5ed-157">Minor updates only</span></span> |
| <span data-ttu-id="6c5ed-158">สัปดาห์ของวันที่ 23 เดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="6c5ed-158">Week of December 23</span></span> | <span data-ttu-id="6c5ed-159">ไม่มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-159">No updates</span></span> |
| <span data-ttu-id="6c5ed-160">สัปดาห์ของวันที่ 30 เดือนธันวาคม</span><span class="sxs-lookup"><span data-stu-id="6c5ed-160">Week of December 30</span></span> | <span data-ttu-id="6c5ed-161">ไม่มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-161">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="6c5ed-162">การสื่อสาร</span><span class="sxs-lookup"><span data-stu-id="6c5ed-162">Communications</span></span>

<span data-ttu-id="6c5ed-163">คุณสามารถค้นหาสิ่งที่อยู่ในงานสำหรับทรัพยากรบุคคล และสิ่งที่เราได้นำออกใช้ในสถานที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6c5ed-163">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="6c5ed-164">แผนการทำงาน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="6c5ed-164">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="6c5ed-165">แผนการนำออกใข้ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6c5ed-165">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="6c5ed-166">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="6c5ed-166">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="6c5ed-167">[การค้นหาปัญหาใน Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (สำหรับบักที่เกี่ยวข้องกับแพลตฟอร์มเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-167">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="6c5ed-168">บล็อกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="6c5ed-168">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="6c5ed-169">ชุมชน Human Resources Yammer</span><span class="sxs-lookup"><span data-stu-id="6c5ed-169">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="6c5ed-170">ลักษณะการทำงานการแสดงตัวอย่างในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="6c5ed-170">Preview features in a sandbox environment</span></span>

<span data-ttu-id="6c5ed-171">คุณสามารถตรวจสอบความถูกต้องของลักษณะการแสดงตัวอย่างในสภาพแวดล้อม Sandbox ก่อนที่จะเปิดใช้งานในสภาพแวดล้อมการผลิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-171">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="6c5ed-172">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะใหม่ ดูที่ [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-172">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="6c5ed-173">ลักษณะการทำงานใหม่ทั้งหมดยังคงอยู่ในการแสดงตัวอย่างอย่างน้อย 30 วัน และโดยปกติจะคงอยู่ 30-60 วัน</span><span class="sxs-lookup"><span data-stu-id="6c5ed-173">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="6c5ed-174">ลักษณะการทำงานที่สำคัญโดยทั่วไปจะมีอยู่ในเดือนตุลาคมและเดือนเมษายนของแต่ละปีตามรอบระยะเวลาการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6c5ed-174">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="6c5ed-175">ทันทีที่คุณเห็นความสามารถใหม่ในพื้นที่ทำงาน การจัดการลักษณะการทำงาน คุณสามารถเปิดใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-175">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="6c5ed-176">ลักษณะการทำงานบางอย่างอาจเปิดใช้งานตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6c5ed-176">Some features may be on by default.</span></span>

<span data-ttu-id="6c5ed-177">เมื่อเวลาผ่านไป ลักษณะการทำงานที่สำคัญจะเปิดใช้งานโดยค่าเริ่มต้นและไม่สามารถปิดได้ (ตัวอย่างเช่น พื้นที่ทำงาน การจัดการลักษณะการทำงาน)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-177">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="6c5ed-178">เมื่อมีลักษณะการทำงานที่พร้อมใช้งาน โดยทั่วไปจะสามารถเปิดหรือปิดใช้งานได้ในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="6c5ed-178">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="6c5ed-179">พื้นที่ทำงาน การจัดการลักษณะการทำงาน บ่งชี้ว่าลักษณะการทำงานในการแสดงตัวอย่างจะกลายเป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-179">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="6c5ed-180">โดยปกติแล้ววันที่นี้จะเป็นวันที่ 1 ตุลาคม หรือ 1 เมษายน เพื่อให้สอดคล้องกับแผนการวางจำหน่ายรายย่อย</span><span class="sxs-lookup"><span data-stu-id="6c5ed-180">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="6c5ed-181">คุณไม่สามารถเปิดหรือปิดคุณลักษณะบังคับได้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-181">You can't turn off mandatory features.</span></span> <span data-ttu-id="6c5ed-182">คุณไม่สามารถเปิดและปิดลักษณะการทำงานในสภาพแวดล้อมทั้งหมดได้จนกว่าจะเป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-182">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="6c5ed-183">เราขอแนะนำการแสดงตัวอย่างคุณลักษณะใน Sandbox หรือสภาพแวดล้อมสำหรับการทดลองใช้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-183">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="6c5ed-184">ควรสร้างสำเนาของสภาพแวดล้อมการผลิตปัจจุบัน หรือฐานข้อมูลของคุณให้เป็นสภาพแวดล้อม Sandbox เพื่อให้คุณสามารถได้รับประสบการณ์ที่สมบูรณ์ของลักษณะการทำงานใหม่ ๆ กับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="6c5ed-184">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="6c5ed-185">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดเตรียมสภาพแวดล้อม Sandbox ดูที่ [การจัดเตรียมโครงการทรัพยากรบุคคล](hr-admin-setup-provision.md)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-185">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="6c5ed-186">เมื่อต้องการเอาสภาพแวดล้อมการทอสอบออก ดูที่ [เอาอินสแตนซ์ออก](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-186">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="6c5ed-187">รายงานบัก</span><span class="sxs-lookup"><span data-stu-id="6c5ed-187">Report bugs</span></span>

<span data-ttu-id="6c5ed-188">ในขณะที่กำลังทดสอบลักษณะการทำงานการแสดงตัวอย่าง หรือกำลังลองความสามารถใหม่ ๆ คุณอาจพบรายการที่ไม่ทำงานตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="6c5ed-188">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="6c5ed-189">โปรดรายงานบักใด ๆ ผ่าน [การสนับสนุนของ Microsoft Dynamics 365](https://dynamics.microsoft.com/support/)</span><span class="sxs-lookup"><span data-stu-id="6c5ed-189">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c5ed-190">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="6c5ed-190">See also</span></span>

- [<span data-ttu-id="6c5ed-191">แผนการนำออกใช้ Dynamics 365 และ Power Platform</span><span class="sxs-lookup"><span data-stu-id="6c5ed-191">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="6c5ed-192">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="6c5ed-192">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="6c5ed-193">นโยบายวงจรการใช้งานซอฟต์แวร์</span><span class="sxs-lookup"><span data-stu-id="6c5ed-193">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

