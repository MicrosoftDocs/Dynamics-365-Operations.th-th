---
title: จัดการคุณลักษณะ
description: หัวข้อนี้อธิบายวิธีการที่ทำให้ผู้ดูแลระบบสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างได้ใน Microsoft Dynamics 365 Talent และจะแสดงรายการคุณลักษณะที่ถูกเปิดใช้งานสำหรับการแสดงตัวอย่างในขณะนี้
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
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124807"
---
# <a name="manage-features"></a><span data-ttu-id="859ed-103">จัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="859ed-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="859ed-104">เนื่องจากเป็นส่วนหนึ่งของการเปิดตัวความสามารถของการจัดการทุนมนุษย์ (HCM) สำหรับ Microsoft Dynamics 365 Human Resources เราต้องการให้ลูกค้าพบกับคุณลักษณะใหม่โดยเร็วที่สุด</span><span class="sxs-lookup"><span data-stu-id="859ed-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="859ed-105">ผู้ดูและระบบสามารถดูและใช้งานคุณลักษณะการแสดงตัวอย่างในสภาพแวดล้อมดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="859ed-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="859ed-106">คุณลักษณะเหล่านี้ใกล้จะพร้อมสำหรับความพร้อมใช้งานทั่วไป และได้ผ่านการทดสอบอย่างครอบคลุมแล้ว</span><span class="sxs-lookup"><span data-stu-id="859ed-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="859ed-107">เรากำลังมองหาความคิดเห็นและการตรวจสอบความถูกต้องของลูกค้าในขั้นตอนสุดท้าย ก่อนที่เราจะนำคุณลักษณะเหล่านี้ออกไปใช้งานสำหรับความพร้อมใช้งานทั่วไป</span><span class="sxs-lookup"><span data-stu-id="859ed-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="859ed-108">หัวข้อนี้อธิบายวิธีการที่ทำให้คุณสามารถเปิดใช้งานคุณลักษณะแสดงตัวอย่าง และแสดงรายการคุณลักษณะที่พร้อมใช้งานสำหรับการแสดงตัวอย่างในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="859ed-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="859ed-109">รายการนี้จะถูกอัพเดต เมื่อคุณลักษณะถูกนำไปใช้ในความพร้อมใช้งานทั่วไป และเมื่อมีการนำคุณลักษณะใหม่ออกใช้เพื่อแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="859ed-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="859ed-110">ไม่มีการแจ้งเตือนให้ทราบ เมื่อมีการนำคุณลักษณะใหม่มาแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="859ed-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="859ed-111">ผู้ใช้จะเริ่มต้นเห็นคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="859ed-111">Users will just start to see the features.</span></span> <span data-ttu-id="859ed-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะใหม่ๆ ใน Talent ดู [มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent](./whats-new.md) และ [บันทึกย่อประจำรุ่นของ Dynamics 365 และ Power Platform](https://docs.microsoft.com/business-applications-release-notes)</span><span class="sxs-lookup"><span data-stu-id="859ed-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="859ed-113">เปิดใช้งาน หรือปิดใช้งานคุณลักษณะการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="859ed-113">Enable or disable preview features</span></span>

<span data-ttu-id="859ed-114">เมื่อต้องการเข้าถึงคุณลักษณะการแสดงตัวอย่าง คุณต้องเปิดใช้งานในสภาพแวดล้อมของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="859ed-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="859ed-115">การเปิดหรือปิดใช้งานคุณลักษณะการแสดงตัวอย่างเป็นแบบเฉพาะกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="859ed-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="859ed-116">เมื่อคุณเปิดการตั้งค่า **คุณลักษณะการแสดงตัวอย่าง** คุณเปิดใช้งานคุณลักษณะการแสดงตัวอย่างสำหรับผู้ใช้ทั้งหมดในองค์กรของคุณที่อยู่ในสภาพแวดล้อมนั้น</span><span class="sxs-lookup"><span data-stu-id="859ed-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="859ed-117">เมื่อคุณปิดการตั้งค่า คุณจะปิดใช้งานคุณลักษณะการแสดงตัวอย่าง และทำให้ไม่สามารถเข้าถึงผู้ใช้ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="859ed-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="859ed-118">คุณลักษณะการแสดงตัวอย่างมีการสนับสนุนที่จำกัดใน Talent</span><span class="sxs-lookup"><span data-stu-id="859ed-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="859ed-119">อาจใช้ความเป็นส่วนตัวและมาตรการด้านความปลอดภัยน้อยลง และจะไม่ถูกรวมอยู่ในข้อตกลงระดับการบริการ Talent (SLA)</span><span class="sxs-lookup"><span data-stu-id="859ed-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="859ed-120">คุณไม่ควรใช้คุณลักษณะการแสดงตัวอย่างในการประมวลผลข้อมูลส่วนบุคคล (นั่นคือ ข้อมูลใดๆ ที่สามารถระบุตัวคุณได้) หรือในการประมวลผลข้อมูลอื่นๆ ที่ขึ้นอยู่กับความต้องการปฏิบัติตามกฎหมาย หรือตามข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="859ed-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="859ed-121">ดึงดูด</span><span class="sxs-lookup"><span data-stu-id="859ed-121">Attract</span></span>

1. <span data-ttu-id="859ed-122">ลงชื่อเข้าใช้ Microsoft Dynamics 365 Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="859ed-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="859ed-123">ในเมนู **ตั้งค่า** (สัญลักษณ์เกียร์) ในมุมบนด้านขวา เลือก **ศูนย์ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="859ed-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="859ed-124">บนแท็บ **การจัดการคุณลักษณะ** เลือกตัวเลือกถัดจาก **คุณลักษณะการแสดงตัวอย่าง** เพื่อให้กลายเป็นสีฟ้า และกล่าวว่า **เปิด**</span><span class="sxs-lookup"><span data-stu-id="859ed-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![เปิดใช้งานคุณลักษณะการแสดงตัวอย่างใน Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="859ed-126">เลือกหรือยกเลิกการเลือกของคุณลักษณะการแสดงตัวอย่างแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="859ed-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="859ed-127">ถ้าคุณไม่ได้ทำอะไรเลย คุณสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างทั้งหมดที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="859ed-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="859ed-128">รีเฟรชเบราเซอร์ของคุณเพื่อเริ่มต้นดูคุณลักษณะใหม่</span><span class="sxs-lookup"><span data-stu-id="859ed-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="859ed-129">ผู้ใช้ใดๆ ที่เข้าสู่ระบบอยู่แล้ว จะเห็นคุณลักษณะในครั้งถัดไปที่พวกเขาเข้าสู่ระบบ หรือพวกเขาสามารถรีเฟรชเบราเซอร์ของพวกเขาเพื่อดูคุณลักษณะโดยทันทีได้</span><span class="sxs-lookup"><span data-stu-id="859ed-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="859ed-130">คุณลักษณะการแสดงตัวอย่างบางรายการอาจต้องการการตั้งค่าคอนฟิกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="859ed-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="859ed-131">ทำตามลิงค์ที่อยู่ถัดจากคุณลักษณะการแสดงตัวอย่างเพื่อทำให้การตั้งค่าเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="859ed-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="859ed-132">ผลป้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="859ed-132">Feedback</span></span>

<span data-ttu-id="859ed-133">เราต้องการได้ยินจากคุณเกี่ยวกับประสบการณ์ของคุณกับคุณลักษณะการแสดงตัวอย่างใดๆ เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="859ed-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="859ed-134">เราขอสนับสนุนให้คุณลงรายการบัญชีคำติชมของคุณอย่างสม่ำเสมอบนไซต์ต่อไปนี้ เมื่อคุณใช้รายการเหล่านี้หรือคุณลักษณะอื่นใดๆ :</span><span class="sxs-lookup"><span data-stu-id="859ed-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="859ed-135">[ชุมชน](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – ไซต์นี้เป็นทรัพยากรที่สำคัญที่ผู้ใช้สามารถอธิบายกรณีที่ใช้ ถามคำถาม และขอความช่วยเหลือของชุมชน</span><span class="sxs-lookup"><span data-stu-id="859ed-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="859ed-136">แจ้งให้เราทราบเกี่ยวกับคุณลักษณะที่คุณต้องการดูในผลิตภัณฑ์ และแจ้งให้เราทราบเกี่ยวกับการเปลี่ยนแปลงใดๆ ที่คุณคิดว่าเราควรจะทำต่อคุณลักษณะที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="859ed-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="859ed-137">แนะนำแนวคิดเกี่ยวกับผลิตภัณฑ์ในไซต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="859ed-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="859ed-138">แนวคิด Attract</span><span class="sxs-lookup"><span data-stu-id="859ed-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="859ed-139">แนวคิด Onboard</span><span class="sxs-lookup"><span data-stu-id="859ed-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="859ed-140">ต้องแน่ใจว่าคุณไม่ได้รวมข้อมูลส่วนบุคคล (ข้อมูลใดๆ ที่สามารถระบุตัวคุณได้) ในความคิดเห็นของคุณ หรือการส่งการตรวจทานผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="859ed-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="859ed-141">ข้อมูลที่ถูกรวบรวมอาจถูกวิเคราะห์เพิ่มเติม และจะไม่ถูกใช้เพื่อตอบสนองคำขอภายใต้กฎหมายความเป็นส่วนตัวที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="859ed-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="859ed-142">ข้อมูลส่วนบุคคลที่ถูกเก็บแยกต่างหากภายใต้โปรแกรมเหล่านี้มีผลต่อ [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="859ed-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="859ed-143">คั่นหัวข้อนี้ และลตรวจสอบย้อนหลังบ่อยๆ เพื่อคอยติดตามสถานการณ์ปัจจุบันเกี่ยวกับคุณลักษณะการทำงานใหม่ เมื่อเรานำออกใช้</span><span class="sxs-lookup"><span data-stu-id="859ed-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="859ed-144">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="859ed-144">See also</span></span>

- [<span data-ttu-id="859ed-145">ลอง หรือซื้อแอป Talent</span><span class="sxs-lookup"><span data-stu-id="859ed-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="859ed-146">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="859ed-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="859ed-147">แผนการรีลีส</span><span class="sxs-lookup"><span data-stu-id="859ed-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="859ed-148">รับการสนับสนุนสำหรับ Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="859ed-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
