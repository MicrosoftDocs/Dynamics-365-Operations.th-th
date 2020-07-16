---
title: ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่
description: หัวข้อนี้อธิบายวิธีการปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)
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
ms.openlocfilehash: 00f35b516dbf6ab4d4d9171c84a16b89f6afe832
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533286"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="78188-103">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="78188-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="78188-104">หัวข้อนี้อธิบายวิธีการปรับใช้ไซต์อีคอมเมิร์ซใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="78188-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="78188-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="78188-105">Overview</span></span>

<span data-ttu-id="78188-106">Microsoft Dynamics Lifecycle Services (LCS) เป็นพื้นที่ทำงานที่ใช้ร่วมกันบน Cloud ซึ่งคู่ค้าและลูกค้าสามารถใช้เพื่อการจัดการโครงการและ สภาพแวดล้อมต่าง ๆ ดูข้อมูลล่าสุดเกี่ยวกับผลิตภัณฑ์และลักษณะการทำงานของ Microsoft Dynamics และ สร้าง ติดตาม และเรียกดูเหตุการณ์สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="78188-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="78188-107">ลักษณะการทำงานในการจัดการอีคอมเมิร์ซถูกรวมเข้ากับ LCS</span><span class="sxs-lookup"><span data-stu-id="78188-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="78188-108">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับ LCS โปรดดูที่ [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)</span><span class="sxs-lookup"><span data-stu-id="78188-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="78188-109">เริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="78188-109">Get started</span></span>

<span data-ttu-id="78188-110">ก่อนที่คุณจะสามารถเริ่มต้นการใช้งานอีคอมเมิร์ซ คุณต้องเริ่มต้นโครงการ สภาพแวดล้อม และ Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="78188-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="78188-111">เมื่อต้องการทำการเริ่มต้นใน LCS คุณต้องได้รับอนุญาตสำหรับบทบาทของเจ้าของโครงการ หรือผู้จัดการสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="78188-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="78188-112">รองรับโทโพโลยีสภาพแวดล้อมการผลิตและ Sandbox</span><span class="sxs-lookup"><span data-stu-id="78188-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="78188-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)</span><span class="sxs-lookup"><span data-stu-id="78188-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="78188-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCSU ให้ดูที่ [เริ่มต้น Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)</span><span class="sxs-lookup"><span data-stu-id="78188-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="78188-115">ตั้งค่าเพื่อเริ่มต้นใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="78188-115">Initialize e-Commerce</span></span>

<span data-ttu-id="78188-116">ใช้ขั้นตอนต่อไปนี้เพื่อเตรียมใช้งานลักษณะการทำงานอีคอมเมิร์ซในสภาพแวดล้อมที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="78188-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="78188-117">ก่อนที่คุณจะเริ่มต้นโปรดตรวจสอบให้แน่ใจว่าคุณมีข้อมูลที่จำเป็นดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="78188-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="78188-118">RCSU ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="78188-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="78188-119">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับ admins ของระบบอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="78188-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="78188-120">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับผู้ดูแลระบบการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="78188-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="78188-121">โดเมนที่จะเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="78188-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="78188-122">นอกจากนี้คุณยังสามารถรวบรวมข้อมูลเสริมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="78188-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="78188-123">Azure AD ข้อมูลธุรกิจ-ผู้บริโภค (B2C):</span><span class="sxs-lookup"><span data-stu-id="78188-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="78188-124">ชื่อผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="78188-124">Tenant Name.</span></span>
    - <span data-ttu-id="78188-125">รหัสไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="78188-125">Client ID.</span></span>
    - <span data-ttu-id="78188-126">โดเมนที่กำหนดเองสำหรับล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="78188-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="78188-127">ตอบ URL</span><span class="sxs-lookup"><span data-stu-id="78188-127">Reply URL.</span></span>
    - <span data-ttu-id="78188-128">รหัสนโยบายการลงทะเบียนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="78188-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="78188-129">รหัสนโยบายการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="78188-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="78188-130">แก้ไขรหัสนโยบายโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="78188-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="78188-131">คุณสามารถเพิ่มข้อมูลนี้ในภายหลังได้ โดยใช้คำขอบริการ</span><span class="sxs-lookup"><span data-stu-id="78188-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="78188-132">หลังจากที่คุณรวบรวมข้อมูลที่จำเป็นแล้ว ให้ทำตามขั้นตอนต่อไปนี้เพื่อเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="78188-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="78188-133">ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="78188-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="78188-134">เปิดโครงการที่มีสภาพแวดล้อมที่คุณต้องการเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="78188-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="78188-135">ในส่วนของ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="78188-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="78188-136">ภายใต้ **ลักษณะการของสภาพแวดล้อม** เลือกลิงก์ **การจัดการ Retail**</span><span class="sxs-lookup"><span data-stu-id="78188-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="78188-137">บนแท็บ **อีคอมเมิร์ซ** ให้เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="78188-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="78188-138">กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณต้องป้อนข้อมูลที่จำเป็นสำหรับการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="78188-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="78188-139">กรอกข้อมูลที่จำเป็นแล้วไปที่หน้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="78188-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="78188-140">บนหน้าถัดไป กรอกข้อมูลที่จำเป็นแล้วกดปุ่มยืนยันฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="78188-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="78188-141">คุณกลับไปที่แท็บ **อีคอมเมิร์ซ** ซึ่งคุณควรเห็นการเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="78188-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="78188-142">เมื่อต้องการดูสถานะการเริ่มต้น ให้ **รีเฟรช** หรือย้อนกลับไปที่แท็บ **อีคอมเมิร์ซ** ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="78188-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="78188-143">เมื่อมีการเริ่มต้นอีคอมเมิร์ซจาก LCS ระบบจะกล่าวถึงส่วนประกอบต่างๆที่จำเป็นสำหรับอีคอมเมิร์ซและเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="78188-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="78188-144">หลังจากเสร็จสิ้นการเตรียมใช้งานแล้ว แท็บ **e-Commerce** บนหน้า **การจัดการค้าปลีก** ได้รับการปรับปรุงเพื่อแสดงถึงการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="78188-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="78188-145">หน้าแสดงการปรับใช้การกำหนดเองล่าสุด และสถานะของการปรับใช้ที่กำลังทำงานอยู่อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="78188-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="78188-146">นอกจากนี้ยังมีลิงก์ไปยังไซต์ e-Commerce และตัวสร้างไซต์ e-Commerce ที่มีการเขียนไซต์</span><span class="sxs-lookup"><span data-stu-id="78188-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="78188-147">การเข้าใช้ตัวสร้างไซต์ </span><span class="sxs-lookup"><span data-stu-id="78188-147">Access site builder</span></span>

<span data-ttu-id="78188-148">การเข้าใช้ตัวสร้างไซต์ ไปที่แท็บ **e-Commerce** บนหน้า **การจัดการขายปลีก** ใน LCS และเลือกลิงก์ **เครื่องมือการจัดการไซต์ e-Commerce** </span><span class="sxs-lookup"><span data-stu-id="78188-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="78188-149">ในหน้าเริ่มต้นของตัวสร้างไซต์จะแสดงมุมมองระดับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="78188-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="78188-150">จากหน้านี้ คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="78188-150">From this page, you can:</span></span>

- <span data-ttu-id="78188-151">ปรับเปลี่ยนการตั้งค่าระดับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="78188-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="78188-152">นำทางไปยังไซต์ใด ๆ ที่คุณสร้างขึ้นและมีสิทธิ์ดู</span><span class="sxs-lookup"><span data-stu-id="78188-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="78188-153">คุณลักษณะการตรวจสอบการเข้าถึง เช่น การควบคุมและการรายงาน</span><span class="sxs-lookup"><span data-stu-id="78188-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="78188-154">สร้างไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="78188-154">Create a new site.</span></span> <span data-ttu-id="78188-155">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างไซต์ใหม่ ดู [สร้างไซต์ e-Commerce](create-ecommerce-site.md) </span><span class="sxs-lookup"><span data-stu-id="78188-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="78188-156">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="78188-156">Additional resources</span></span>

[<span data-ttu-id="78188-157">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="78188-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="78188-158">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="78188-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="78188-159">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="78188-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="78188-160">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="78188-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="78188-161">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="78188-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="78188-162">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="78188-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="78188-163">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="78188-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="78188-164">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="78188-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="78188-165">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="78188-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="78188-166">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="78188-166">Enable location-based store detection</span></span>](enable-store-detection.md)
