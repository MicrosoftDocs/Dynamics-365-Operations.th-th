---
title: การแก้ไขปัญหาการรวม LinkedIn กับ Microsoft Dynamics 365 Talent - Attract
description: หัวข้อนี้อธิบายถึงวิธีการแก้ไขปัญหาเมื่อคุณพยายามลงประกาศงานไปยัง LinkedIn จาก Microsoft Dynamics 365 Talent - Attract
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: b031fd95d2e7fc8405ad96139779091e00bb4d46
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551483"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="4603f-103">การแก้ไขปัญหาการรวม LinkedIn กับ Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="4603f-103">Troubleshoot integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4603f-104">ใช้ข้อมูลต่อไปนี้เพื่อช่วยแก้ไขปัญหาที่คุณอาจมี เมื่อคุณพยายามลงประกาศงานไปยัง LinkedIn จาก Microsoft Dynamics 365 Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="4603f-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="4603f-105">คุณไม่สามารถลงชื่อเข้าใช้ LinkedIn จาก Attract</span><span class="sxs-lookup"><span data-stu-id="4603f-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="4603f-106">หากคุณกำลังประสบปัญหาในการลงชื่อเข้าใช้ LinkedIn จาก Attract ให้ลองทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4603f-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="4603f-107">ตรวจสอบว่าข้อมูลประจำตัวของ LinkedIn ที่คุณป้อนใน Attract ใช้ได้และถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4603f-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="4603f-108">ถ้าข้อมูลประจำตัวใช้ได้และถูกต้อง ติดต่อ [ฝ่ายสนับสนุนของ LinkedIn](https://www.linkedin.com/help/linkedin)</span><span class="sxs-lookup"><span data-stu-id="4603f-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="4603f-109">ถ้าปัญหายังคงอยู่ ติดต่อ [ฝ่ายสนับสนุนของ Microsoft](./talent-support.md)</span><span class="sxs-lookup"><span data-stu-id="4603f-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="4603f-110">ประกาศงานจาก Attract ไม่ปรากฏบน LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4603f-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="4603f-111">ถ้างานของคุณไม่ปรากฏบน LinkedIn หลังจาก 24 ชั่วโมง ให้ลองทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4603f-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="4603f-112">ตรวจสอบให้แน่ใจว่ารหัสของบริษัท LinkedIn ของคุณแม็ปไปยังหน้าของบริษัท LinkedIn ของคุณ และป้อนไว้อย่างถูกต้องในศูนย์การจัดการ Attract</span><span class="sxs-lookup"><span data-stu-id="4603f-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="4603f-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนการตั้งค่า LinkedIn ในศูนย์การจัดการ ให้ดูที่ [ตั้งค่าการรวมกับ LinkedIn](attract-admin-linkedin.md)</span><span class="sxs-lookup"><span data-stu-id="4603f-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="4603f-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสบริษัท LinkedIn โปรดดูที่ [การเชื่อมโยงรหัสบริษัท Linkedin กับบอร์ดงาน Linkedin - คำถามที่ถามบ่อย](https://www.linkedin.com/help/linkedin/answer/98972)</span><span class="sxs-lookup"><span data-stu-id="4603f-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="4603f-115">ตรวจสอบรายละเอียดงานบน LinkedIn เพื่อให้แน่ใจว่าที่อยู่เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="4603f-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="4603f-116">เมื่อต้องการลงประกาศงานให้สมบูรณ์ LinkedIn ต้องการอย่างน้อยเมืองและประเทศหรือภูมิภาคของงาน</span><span class="sxs-lookup"><span data-stu-id="4603f-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="4603f-117">ตรวจสอบให้แน่ใจว่างานไม่ซ้ำกับงานอื่นที่มีการลงประกาศแล้วใน LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4603f-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="4603f-118">LinkedIn จะไม่ลงประกาศงานที่ซ้ำกับช่องงานพิเศษของ LinkedIn หรือรายการที่จำกัดจากแหล่งที่มาอื่น</span><span class="sxs-lookup"><span data-stu-id="4603f-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="4603f-119">ตรวจสอบว่าบุคคลอื่นในบริษัทของคุณยังไม่ได้ลงประกาศงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4603f-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="4603f-120">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4603f-120">See also</span></span>

[<span data-ttu-id="4603f-121">FAQ เกี่ยวกับ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4603f-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="4603f-122">ลงประกาศงานใน LinkedIn จาก Attract</span><span class="sxs-lookup"><span data-stu-id="4603f-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="4603f-123">จัดหาผู้สมัครด้วย LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="4603f-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="4603f-124">สร้างงาน</span><span class="sxs-lookup"><span data-stu-id="4603f-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="4603f-125">แก้ไขปัญหาการรวมกับ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4603f-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
