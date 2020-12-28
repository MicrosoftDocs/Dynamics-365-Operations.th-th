---
title: ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่
description: หัวข้อนี้อธิบายวิธีการปรับใช้ไซต์อีคอมเมิร์ซ Dynamics 365 Commerce ใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 157dc8225e5bbf9338a1b5a79a2880e8a8c4bf10
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517293"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="8f88e-103">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="8f88e-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8f88e-104">หัวข้อนี้อธิบายวิธีการปรับใช้ไซต์อีคอมเมิร์ซ Dynamics 365 Commerce ใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8f88e-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="8f88e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8f88e-105">Overview</span></span>

<span data-ttu-id="8f88e-106">Microsoft Dynamics Lifecycle Services (LCS) เป็นพื้นที่ทำงานที่ใช้ร่วมกันบน Cloud ซึ่งคู่ค้าและลูกค้าสามารถใช้เพื่อการจัดการโครงการและ สภาพแวดล้อมต่าง ๆ ดูข้อมูลล่าสุดเกี่ยวกับผลิตภัณฑ์และลักษณะการทำงานของ Microsoft Dynamics และ สร้าง ติดตาม และเรียกดูเหตุการณ์สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="8f88e-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="8f88e-107">คุณลักษณะการจัดการอีคอมเมิร์ซถูกรวมเข้ากับ LCS</span><span class="sxs-lookup"><span data-stu-id="8f88e-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="8f88e-108">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับ LCS โปรดดูที่ [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)</span><span class="sxs-lookup"><span data-stu-id="8f88e-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="8f88e-109">เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8f88e-109">Get started</span></span>

<span data-ttu-id="8f88e-110">ก่อนที่คุณจะสามารถเริ่มต้นการใช้งานอีคอมเมิร์ซ คุณต้องเริ่มต้นโครงการ สภาพแวดล้อม และ Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="8f88e-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="8f88e-111">เมื่อต้องการทำการเริ่มต้นใน LCS คุณต้องได้รับอนุญาตสำหรับบทบาทของเจ้าของโครงการ หรือผู้จัดการสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8f88e-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="8f88e-112">รองรับโทโพโลยีสภาพแวดล้อมการผลิตและ Sandbox</span><span class="sxs-lookup"><span data-stu-id="8f88e-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="8f88e-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)</span><span class="sxs-lookup"><span data-stu-id="8f88e-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="8f88e-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCSU ให้ดูที่ [เริ่มต้น Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)</span><span class="sxs-lookup"><span data-stu-id="8f88e-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="8f88e-115">เตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8f88e-115">Initialize e-commerce</span></span>

<span data-ttu-id="8f88e-116">ใช้กระบวนงานนี้เพื่อเตรียมใช้งานคุณลักษณะอีคอมเมิร์ซในสภาพแวดล้อมที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8f88e-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="8f88e-117">ก่อนที่คุณจะเริ่มต้นโปรดตรวจสอบให้แน่ใจว่าคุณมีข้อมูลที่จำเป็นดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8f88e-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="8f88e-118">RCSU ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="8f88e-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="8f88e-119">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับผู้ดูแลระบบอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8f88e-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="8f88e-120">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับผู้ดูแลระบบการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="8f88e-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="8f88e-121">โดเมนที่จะเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8f88e-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="8f88e-122">นอกจากนี้คุณยังสามารถรวบรวมข้อมูลเสริมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8f88e-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="8f88e-123">Azure AD ข้อมูลธุรกิจ-ผู้บริโภค (B2C):</span><span class="sxs-lookup"><span data-stu-id="8f88e-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="8f88e-124">ชื่อผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="8f88e-124">Tenant Name.</span></span>
    - <span data-ttu-id="8f88e-125">รหัสไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="8f88e-125">Client ID.</span></span>
    - <span data-ttu-id="8f88e-126">โดเมนที่กำหนดเองสำหรับล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="8f88e-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="8f88e-127">ตอบ URL</span><span class="sxs-lookup"><span data-stu-id="8f88e-127">Reply URL.</span></span>
    - <span data-ttu-id="8f88e-128">รหัสนโยบายการลงทะเบียนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8f88e-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="8f88e-129">รหัสนโยบายการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="8f88e-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="8f88e-130">แก้ไขรหัสนโยบายโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="8f88e-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="8f88e-131">คุณสามารถเพิ่มข้อมูลนี้ในภายหลังได้ โดยใช้คำขอบริการ</span><span class="sxs-lookup"><span data-stu-id="8f88e-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="8f88e-132">หลังจากที่คุณรวบรวมข้อมูลที่จำเป็นแล้ว ให้ทำตามขั้นตอนต่อไปนี้เพื่อเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8f88e-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="8f88e-133">ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="8f88e-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="8f88e-134">เปิดโครงการที่มีสภาพแวดล้อมที่คุณต้องการเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8f88e-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="8f88e-135">ในส่วนของ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8f88e-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="8f88e-136">ภายใต้ **ลักษณะการของสภาพแวดล้อม** เลือกลิงก์ **การจัดการ Retail**</span><span class="sxs-lookup"><span data-stu-id="8f88e-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="8f88e-137">บนแท็บ **อีคอมเมิร์ซ** ให้เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="8f88e-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="8f88e-138">กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณต้องป้อนข้อมูลที่จำเป็นสำหรับการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="8f88e-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="8f88e-139">กรอกข้อมูลที่จำเป็นแล้วไปที่หน้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="8f88e-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="8f88e-140">บนหน้าถัดไป กรอกข้อมูลที่จำเป็นแล้วกดปุ่มยืนยันฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="8f88e-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="8f88e-141">คุณกลับไปที่แท็บ **อีคอมเมิร์ซ** ซึ่งคุณควรเห็นการเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="8f88e-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="8f88e-142">เมื่อต้องการดูสถานะการเริ่มต้น ให้ **รีเฟรช** หรือย้อนกลับไปที่แท็บ **อีคอมเมิร์ซ** ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8f88e-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="8f88e-143">เมื่อมีการเตรียมใช้งานอีคอมเมิร์ซจาก LCS ระบบจะสำรองส่วนประกอบต่างๆ ที่จำเป็นสำหรับอีคอมเมิร์ซและเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8f88e-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="8f88e-144">หลังจากเสร็จสิ้นการเตรียมใช้งานแล้ว แท็บ **e-Commerce** บนหน้า **การจัดการค้าปลีก** ได้รับการปรับปรุงเพื่อแสดงถึงการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8f88e-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="8f88e-145">หน้าแสดงการปรับใช้การกำหนดเองล่าสุด และสถานะของการปรับใช้ที่กำลังทำงานอยู่อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="8f88e-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="8f88e-146">นอกจากนี้ ยังมีลิงก์ไปยังไซต์อีคอมเมิร์ซและตัวสร้างไซต์อีคอมเมิร์ซที่มีการเขียนไซต์</span><span class="sxs-lookup"><span data-stu-id="8f88e-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="8f88e-147">เข้าถึงตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="8f88e-147">Access Commerce site builder</span></span>

<span data-ttu-id="8f88e-148">ในการเข้าถึงตัวสร้างไซต์ Commerce ไปที่แท็บ **อีคอมเมิร์ซ** บนหน้า **การจัดการขายปลีก** ใน LCS และเลือกลิงก์ **เครื่องมือการจัดการไซต์อีคอมเมิร์ซ**</span><span class="sxs-lookup"><span data-stu-id="8f88e-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="8f88e-149">ในหน้าเริ่มต้นของตัวสร้างไซต์จะแสดงมุมมองระดับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="8f88e-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="8f88e-150">จากหน้านี้ คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="8f88e-150">From this page, you can:</span></span>

- <span data-ttu-id="8f88e-151">ปรับเปลี่ยนการตั้งค่าระดับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="8f88e-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="8f88e-152">นำทางไปยังไซต์ใด ๆ ที่คุณสร้างขึ้นและมีสิทธิ์ดู</span><span class="sxs-lookup"><span data-stu-id="8f88e-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="8f88e-153">คุณลักษณะการตรวจสอบการเข้าถึง เช่น การควบคุมและการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8f88e-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="8f88e-154">สร้างไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="8f88e-154">Create a new site.</span></span> <span data-ttu-id="8f88e-155">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างไซต์ใหม่ ดู [สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="8f88e-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="8f88e-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8f88e-156">Additional resources</span></span>

[<span data-ttu-id="8f88e-157">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="8f88e-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8f88e-158">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8f88e-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8f88e-159">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="8f88e-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8f88e-160">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="8f88e-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8f88e-161">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="8f88e-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8f88e-162">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="8f88e-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8f88e-163">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8f88e-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8f88e-164">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="8f88e-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8f88e-165">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="8f88e-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8f88e-166">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8f88e-166">Enable location-based store detection</span></span>](enable-store-detection.md)
