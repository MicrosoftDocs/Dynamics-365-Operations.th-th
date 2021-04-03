---
title: อัปเดตกระบวนการ
description: Microsoft Dynamics 365 Human Resources เป็นซอฟต์แวร์จริงในฐานะบริการ (SaaS) ที่ให้การอัปเดตของการบริการระยะไกลที่ต่อเนื่องสำหรับแอพลิเคชันและการเปลี่ยนแปลงแพลตฟอร์ม
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27561bfd9cb4f115cc507954c837ea93f9c93b72
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466843"
---
# <a name="update-process"></a><span data-ttu-id="87363-103">อัปเดตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="87363-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="87363-104">Microsoft Dynamics 365 Human Resources เป็นซอฟต์แวร์จริงในฐานะบริการ (SaaS) ที่มีการอัปเดตของการบริการระยะไกลที่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="87363-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="87363-105">การอัปเดตเหล่านี้จะมีการเปลี่ยนแปลงทั้งโปรแกรมประยุกต์และแพลตฟอร์ม ซึ่งมักให้การปรับปรุงที่สำคัญแก่การบริการ รวมถึงการอัปเดตตามข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="87363-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="87363-106">นโยบายการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="87363-106">Update policy</span></span>

<span data-ttu-id="87363-107">การอัปเดตจะถูกนำออกใช้เป็นช่วงเวลาตามปกติกับสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="87363-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="87363-108">ทรัพยากรบุคคลได้รับการสนับสนุนตาม [นโยบายของ Microsoft Lifecycle](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ซึ่งให้แนวทางปฏิบัติอย่างต่อเนื่อง และคาดการณ์ได้สำหรับความพร้อมในการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="87363-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="87363-109">ระยะความถี่การนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="87363-109">Release cadence</span></span> 

<span data-ttu-id="87363-110">การอัปเดตทรัพยากรบุคคลจะใช้กับสภาพแวดล้อมทั้งหมดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="87363-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="87363-111">ทรัพยากรบุคคลมีการนำออกใช้สองชนิดดังนี้</span><span class="sxs-lookup"><span data-stu-id="87363-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="87363-112">**การปรับปรุงบริการ**: การปรับปรุงเกิดขึ้นทุกสองสัปดาห์ซึ่งรวมถึงการแก้ไขปัญหาบักและคุณลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="87363-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="87363-113">การอัปเดตบริการมีการอัปเดตแพลตฟอร์มที่ใช้ได้เมื่อมีการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="87363-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="87363-114">เพื่อให้ได้แนวคิดเมื่อนำออกใช้การอัปเดตแพลตฟอร์ม ดูที่ [ตารางที่ 3: การนำออกใช้แพลตฟอร์ม](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases)</span><span class="sxs-lookup"><span data-stu-id="87363-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="87363-115">การปรับปรุงรายสองอาทิตย์มีการเปิดตัวทั่วโลกที่มีการแบ่งระยะทั่วทั้งภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="87363-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="87363-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการปรับปรุงรายสองสัปดาห์ ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources](hr-admin-whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="87363-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="87363-117">ศูนย์ข้อมูลที่ได้รับการสนับสนุนทั้งหมดมีการปรับปรุงทุกสองสัปดาห์ เว้นแต่จะมีการระบุไว้เป็นอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="87363-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="87363-118">ภูมิภาคสหรัฐอเมริกา ออสเตรเลีย ยุโรป อังกฤษ เอเชีย และแคนาดา รวมอยู่ในการปรับปรุงรายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="87363-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="87363-119">**การอัปเดตโซลูชัน Dataverse**: การอัปเดตเหล่านี้เกิดขึ้นโดยประมาณทุก ๆ 6 สัปดาห์ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="87363-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="87363-120">ซึ่งรวมถึงเอนทิตีใหม่และการเปลี่ยนแปลงที่เกิดขึ้นกับเอนทิตีที่มีอยู่ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="87363-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="87363-121">การปรับปรุงเหล่านี้จะนำออกไปสู่ภูมิภาคเดียวกันกับการปรับปรุงรายสองสัปดาห์ และใช้เวลาประมาณหกสัปดาห์ในการทำซ้ำโดยผ่านศูนย์ข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="87363-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="87363-122">การปรับปรุงโซลูชันอาจสอดคล้องหรืออาจไม่สอดคล้องกับการปรับปรุงการบริการรายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="87363-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="87363-123">การอัปเดตโซลูชันมีอยู่ในศูนย์ข้อมูลทั้งหมดเมื่อมีการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="87363-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="87363-124">ถ้าคุณไม่ต้องการรอให้การอัปเดตจำลองแบบโดยอัตโนมัติ คุณสามารถใช้การอัปเดตใด ๆ เหล่านี้กับสภาพแวดล้อมใด ๆ ในศูนย์ข้อมูลใด ๆ ได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="87363-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="87363-125">เมื่อต้องการ ทรัพยากรบุคคลจะมีชนิดการแก้ไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="87363-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="87363-126">**การแก้ไข (แก้ไขด่วน)**: การแก้ไขปัญหาบักที่อาจเกิดขึ้นทั้งกับหรือนอกเหนือจากการนำออกใช้การปรับปรุงบริการรายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="87363-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="87363-127">**การแก้ไขกรณีฉุกเฉิน**: การแก้ไขด่วนเชิงรุกและเชิงรับมีการทำงานในลักษณะที่เป็นแบบสแตนด์อโลน อาจรวมถึงการเปลี่ยนแปลงเฉพาะการตั้งค่าคอนฟิกหรือการเปลี่ยนแปลงรหัสเพื่อแก้ปัญหาการใช้งานไซต์ที่เริ่มใช้งานจริง และอาจเกิดขึ้นนอกเหนือจากจากการนำออกใช้การปรับปรุงบริการรายสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="87363-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="87363-128">การนำออกใช้มีการตรวจสอบ ทดสอบและตรวจสอบความถูกต้องบนสภาพแวดล้อมภายใน</span><span class="sxs-lookup"><span data-stu-id="87363-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="87363-129">หลังจากที่มีการอนุมัติแล้วแล้ว การสร้างจะถูกนำไปใช้เพื่อการผลิต</span><span class="sxs-lookup"><span data-stu-id="87363-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="87363-130">ข้อยกเว้นของระยะความถี่การนำออกใช้ใน 2020</span><span class="sxs-lookup"><span data-stu-id="87363-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="87363-131">เมื่อต้องการลงบัญชีสำหรับวันหยุด กำหนดการเผยแพร่สำหรับเดือนพฤศจิกายนและธันวาคม 2020 มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="87363-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="87363-132">การเผยแพร่เดือนพฤศจิกายน: 2 พฤศจิกายน - 13 พฤศจิกายน</span><span class="sxs-lookup"><span data-stu-id="87363-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="87363-133">การเผยแพร่เดือนธันวาคม: 30 พฤศจิกายน - 11 ธันวาคม</span><span class="sxs-lookup"><span data-stu-id="87363-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="87363-134">ลำดับการเผยแพร่แบบสองสัปดาห์จะดำเนินการต่อไปตามปกติในวันที่ 11 มกราคม 2021</span><span class="sxs-lookup"><span data-stu-id="87363-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="87363-135">การสื่อสาร</span><span class="sxs-lookup"><span data-stu-id="87363-135">Communications</span></span>

<span data-ttu-id="87363-136">คุณสามารถค้นหาสิ่งที่อยู่ในงานสำหรับทรัพยากรบุคคล และสิ่งที่เราได้นำออกใช้ในสถานที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="87363-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="87363-137">แผนการทำงาน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="87363-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="87363-138">แผนการนำออกใข้ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="87363-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="87363-139">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="87363-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="87363-140">[การค้นหาปัญหาใน Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (สำหรับบักที่เกี่ยวข้องกับแพลตฟอร์มเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="87363-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="87363-141">บล็อกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="87363-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="87363-142">ชุมชน Human Resources Yammer</span><span class="sxs-lookup"><span data-stu-id="87363-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="87363-143">ลักษณะการทำงานการแสดงตัวอย่างในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="87363-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="87363-144">คุณสามารถตรวจสอบความถูกต้องของลักษณะการแสดงตัวอย่างในสภาพแวดล้อม Sandbox ก่อนที่จะเปิดใช้งานในสภาพแวดล้อมการผลิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="87363-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="87363-145">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะใหม่ ดูที่ [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)</span><span class="sxs-lookup"><span data-stu-id="87363-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="87363-146">ลักษณะการทำงานใหม่ทั้งหมดยังคงอยู่ในการแสดงตัวอย่างอย่างน้อย 30 วัน และโดยปกติจะคงอยู่ 30-60 วัน</span><span class="sxs-lookup"><span data-stu-id="87363-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="87363-147">ลักษณะการทำงานที่สำคัญโดยทั่วไปจะมีอยู่ในเดือนตุลาคมและเดือนเมษายนของแต่ละปีตามรอบระยะเวลาการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="87363-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="87363-148">ทันทีที่คุณเห็นความสามารถใหม่ในพื้นที่ทำงาน การจัดการลักษณะการทำงาน คุณสามารถเปิดใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="87363-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="87363-149">ลักษณะการทำงานบางอย่างอาจเปิดใช้งานตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="87363-149">Some features may be on by default.</span></span>

<span data-ttu-id="87363-150">เมื่อเวลาผ่านไป ลักษณะการทำงานที่สำคัญจะเปิดใช้งานโดยค่าเริ่มต้นและไม่สามารถปิดได้ (ตัวอย่างเช่น พื้นที่ทำงาน การจัดการลักษณะการทำงาน)</span><span class="sxs-lookup"><span data-stu-id="87363-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="87363-151">เมื่อมีลักษณะการทำงานที่พร้อมใช้งาน โดยทั่วไปจะสามารถเปิดหรือปิดใช้งานได้ในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="87363-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="87363-152">พื้นที่ทำงาน การจัดการลักษณะการทำงาน บ่งชี้ว่าลักษณะการทำงานในการแสดงตัวอย่างจะกลายเป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="87363-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="87363-153">โดยปกติแล้ววันที่นี้จะเป็นวันที่ 1 ตุลาคม หรือ 1 เมษายน เพื่อให้สอดคล้องกับแผนการวางจำหน่ายรายย่อย</span><span class="sxs-lookup"><span data-stu-id="87363-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="87363-154">คุณไม่สามารถเปิดหรือปิดคุณลักษณะบังคับได้</span><span class="sxs-lookup"><span data-stu-id="87363-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="87363-155">คุณไม่สามารถเปิดและปิดลักษณะการทำงานในสภาพแวดล้อมทั้งหมดได้จนกว่าจะเป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="87363-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="87363-156">เราขอแนะนำการแสดงตัวอย่างคุณลักษณะใน Sandbox หรือสภาพแวดล้อมสำหรับการทดลองใช้</span><span class="sxs-lookup"><span data-stu-id="87363-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="87363-157">ควรสร้างสำเนาของสภาพแวดล้อมการผลิตปัจจุบัน หรือฐานข้อมูลของคุณให้เป็นสภาพแวดล้อม Sandbox เพื่อให้คุณสามารถได้รับประสบการณ์ที่สมบูรณ์ของลักษณะการทำงานใหม่ ๆ กับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="87363-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="87363-158">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดเตรียมสภาพแวดล้อม Sandbox ดูที่ [การจัดเตรียมโครงการทรัพยากรบุคคล](hr-admin-setup-provision.md)</span><span class="sxs-lookup"><span data-stu-id="87363-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="87363-159">เมื่อต้องการเอาสภาพแวดล้อมการทอสอบออก ดูที่ [เอาอินสแตนซ์ออก](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment)</span><span class="sxs-lookup"><span data-stu-id="87363-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="87363-160">รายงานบัก</span><span class="sxs-lookup"><span data-stu-id="87363-160">Report bugs</span></span>

<span data-ttu-id="87363-161">ในขณะที่กำลังทดสอบลักษณะการทำงานการแสดงตัวอย่าง หรือกำลังลองความสามารถใหม่ ๆ คุณอาจพบรายการที่ไม่ทำงานตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="87363-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="87363-162">โปรดรายงานบักใด ๆ ผ่าน [การสนับสนุนของ Microsoft Dynamics 365](https://dynamics.microsoft.com/support/)</span><span class="sxs-lookup"><span data-stu-id="87363-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="87363-163">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="87363-163">See also</span></span>

[<span data-ttu-id="87363-164">แผนการนำออกใช้ Dynamics 365 และ Power Platform</span><span class="sxs-lookup"><span data-stu-id="87363-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="87363-165">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="87363-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="87363-166">นโยบายวงจรการใช้งานซอฟต์แวร์</span><span class="sxs-lookup"><span data-stu-id="87363-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]