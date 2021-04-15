---
title: ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่
description: หัวข้อนี้อธิบายวิธีการปรับใช้ไซต์อีคอมเมิร์ซ Dynamics 365 Commerce ใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0fff5d47d6eb3e08288d17853fcd94f9eab843c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801960"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="81df6-103">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="81df6-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81df6-104">หัวข้อนี้อธิบายวิธีการปรับใช้ไซต์อีคอมเมิร์ซ Dynamics 365 Commerce ใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="81df6-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="81df6-105">Microsoft Dynamics Lifecycle Services (LCS) เป็นพื้นที่ทำงานที่ใช้ร่วมกันบน Cloud ซึ่งคู่ค้าและลูกค้าสามารถใช้เพื่อการจัดการโครงการและ สภาพแวดล้อมต่าง ๆ ดูข้อมูลล่าสุดเกี่ยวกับผลิตภัณฑ์และลักษณะการทำงานของ Microsoft Dynamics และ สร้าง ติดตาม และเรียกดูเหตุการณ์สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="81df6-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="81df6-106">คุณลักษณะการจัดการอีคอมเมิร์ซถูกรวมเข้ากับ LCS</span><span class="sxs-lookup"><span data-stu-id="81df6-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="81df6-107">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับ LCS โปรดดูที่ [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)</span><span class="sxs-lookup"><span data-stu-id="81df6-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="81df6-108">เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="81df6-108">Get started</span></span>

<span data-ttu-id="81df6-109">ก่อนที่คุณจะสามารถเริ่มต้นการใช้งานอีคอมเมิร์ซ คุณต้องเริ่มต้นโครงการ สภาพแวดล้อม และ Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="81df6-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="81df6-110">เมื่อต้องการทำการเริ่มต้นใน LCS คุณต้องได้รับอนุญาตสำหรับบทบาทของเจ้าของโครงการ หรือผู้จัดการสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="81df6-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="81df6-111">รองรับโทโพโลยีสภาพแวดล้อมการผลิตและ Sandbox</span><span class="sxs-lookup"><span data-stu-id="81df6-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="81df6-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)</span><span class="sxs-lookup"><span data-stu-id="81df6-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="81df6-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCSU ให้ดูที่ [เริ่มต้น Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)</span><span class="sxs-lookup"><span data-stu-id="81df6-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="81df6-114">เตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="81df6-114">Initialize e-commerce</span></span>

<span data-ttu-id="81df6-115">ใช้กระบวนงานนี้เพื่อเตรียมใช้งานคุณลักษณะอีคอมเมิร์ซในสภาพแวดล้อมที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="81df6-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="81df6-116">ก่อนที่คุณจะเริ่มต้นโปรดตรวจสอบให้แน่ใจว่าคุณมีข้อมูลที่จำเป็นดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="81df6-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="81df6-117">RCSU ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="81df6-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="81df6-118">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับผู้ดูแลระบบอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="81df6-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="81df6-119">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับผู้ดูแลระบบการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="81df6-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="81df6-120">โดเมนที่จะเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="81df6-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="81df6-121">นอกจากนี้คุณยังสามารถรวบรวมข้อมูลเสริมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="81df6-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="81df6-122">Azure AD ข้อมูลธุรกิจ-ผู้บริโภค (B2C):</span><span class="sxs-lookup"><span data-stu-id="81df6-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="81df6-123">ชื่อผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="81df6-123">Tenant Name.</span></span>
    - <span data-ttu-id="81df6-124">รหัสไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="81df6-124">Client ID.</span></span>
    - <span data-ttu-id="81df6-125">โดเมนที่กำหนดเองสำหรับล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="81df6-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="81df6-126">ตอบ URL</span><span class="sxs-lookup"><span data-stu-id="81df6-126">Reply URL.</span></span>
    - <span data-ttu-id="81df6-127">รหัสนโยบายการลงทะเบียนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="81df6-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="81df6-128">รหัสนโยบายการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="81df6-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="81df6-129">แก้ไขรหัสนโยบายโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="81df6-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="81df6-130">คุณสามารถเพิ่มข้อมูลนี้ในภายหลังได้ โดยใช้คำขอบริการ</span><span class="sxs-lookup"><span data-stu-id="81df6-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="81df6-131">หลังจากที่คุณรวบรวมข้อมูลที่จำเป็นแล้ว ให้ทำตามขั้นตอนต่อไปนี้เพื่อเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="81df6-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="81df6-132">ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="81df6-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="81df6-133">เปิดโครงการที่มีสภาพแวดล้อมที่คุณต้องการเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="81df6-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="81df6-134">ในส่วนของ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="81df6-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="81df6-135">ภายใต้ **ลักษณะการของสภาพแวดล้อม** เลือกลิงก์ **การจัดการ Retail**</span><span class="sxs-lookup"><span data-stu-id="81df6-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="81df6-136">บนแท็บ **อีคอมเมิร์ซ** ให้เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="81df6-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="81df6-137">กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณต้องป้อนข้อมูลที่จำเป็นสำหรับการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="81df6-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="81df6-138">กรอกข้อมูลที่จำเป็นแล้วไปที่หน้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="81df6-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="81df6-139">บนหน้าถัดไป กรอกข้อมูลที่จำเป็นแล้วกดปุ่มยืนยันฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="81df6-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="81df6-140">คุณกลับไปที่แท็บ **อีคอมเมิร์ซ** ซึ่งคุณควรเห็นการเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="81df6-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="81df6-141">เมื่อต้องการดูสถานะการเริ่มต้น ให้ **รีเฟรช** หรือย้อนกลับไปที่แท็บ **อีคอมเมิร์ซ** ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="81df6-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="81df6-142">เมื่อมีการเตรียมใช้งานอีคอมเมิร์ซจาก LCS ระบบจะสำรองส่วนประกอบต่างๆ ที่จำเป็นสำหรับอีคอมเมิร์ซและเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="81df6-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="81df6-143">หลังจากเสร็จสิ้นการเตรียมใช้งานแล้ว แท็บ **e-Commerce** บนหน้า **การจัดการค้าปลีก** ได้รับการปรับปรุงเพื่อแสดงถึงการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="81df6-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="81df6-144">หน้าแสดงการปรับใช้การกำหนดเองล่าสุด และสถานะของการปรับใช้ที่กำลังทำงานอยู่อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="81df6-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="81df6-145">นอกจากนี้ ยังมีลิงก์ไปยังไซต์อีคอมเมิร์ซและตัวสร้างไซต์อีคอมเมิร์ซที่มีการเขียนไซต์</span><span class="sxs-lookup"><span data-stu-id="81df6-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="81df6-146">เข้าถึงตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="81df6-146">Access Commerce site builder</span></span>

<span data-ttu-id="81df6-147">ในการเข้าถึงตัวสร้างไซต์ Commerce ไปที่แท็บ **อีคอมเมิร์ซ** บนหน้า **การจัดการขายปลีก** ใน LCS และเลือกลิงก์ **เครื่องมือการจัดการไซต์อีคอมเมิร์ซ**</span><span class="sxs-lookup"><span data-stu-id="81df6-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="81df6-148">ในหน้าเริ่มต้นของตัวสร้างไซต์จะแสดงมุมมองระดับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="81df6-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="81df6-149">จากหน้านี้ คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="81df6-149">From this page, you can:</span></span>

- <span data-ttu-id="81df6-150">ปรับเปลี่ยนการตั้งค่าระดับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="81df6-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="81df6-151">นำทางไปยังไซต์ใด ๆ ที่คุณสร้างขึ้นและมีสิทธิ์ดู</span><span class="sxs-lookup"><span data-stu-id="81df6-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="81df6-152">คุณลักษณะการตรวจสอบการเข้าถึง เช่น การควบคุมและการรายงาน</span><span class="sxs-lookup"><span data-stu-id="81df6-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="81df6-153">สร้างไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="81df6-153">Create a new site.</span></span> <span data-ttu-id="81df6-154">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างไซต์ใหม่ ดู [สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="81df6-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="81df6-155">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="81df6-155">Additional resources</span></span>

[<span data-ttu-id="81df6-156">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="81df6-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="81df6-157">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="81df6-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="81df6-158">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="81df6-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="81df6-159">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="81df6-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="81df6-160">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="81df6-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="81df6-161">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="81df6-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="81df6-162">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="81df6-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="81df6-163">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="81df6-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="81df6-164">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="81df6-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="81df6-165">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="81df6-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
