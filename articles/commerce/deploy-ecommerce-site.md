---
title: ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่
description: หัวข้อนี้อธิบายวิธีการปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945524"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="00af3-103">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="00af3-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="00af3-104">หัวข้อนี้อธิบายวิธีการปรับใช้ไซต์อีคอมเมิร์ซใหม่โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="00af3-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="00af3-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="00af3-105">Overview</span></span>
    
<span data-ttu-id="00af3-106">Microsoft Dynamics Lifecycle Services (LCS) เป็นพื้นที่ทำงานที่ใช้ร่วมกันบน Cloud ซึ่งคู่ค้าและลูกค้าสามารถใช้เพื่อการจัดการโครงการและ สภาพแวดล้อมต่าง ๆ ดูข้อมูลล่าสุดเกี่ยวกับผลิตภัณฑ์และลักษณะการทำงานของ Microsoft Dynamics และ สร้าง ติดตาม และเรียกดูเหตุการณ์สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="00af3-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="00af3-107">ลักษณะการทำงานในการจัดการอีคอมเมิร์ซถูกรวมเข้ากับ LCS</span><span class="sxs-lookup"><span data-stu-id="00af3-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="00af3-108">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับ LCS โปรดดูที่ [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)</span><span class="sxs-lookup"><span data-stu-id="00af3-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="00af3-109">เริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="00af3-109">Get started</span></span>

<span data-ttu-id="00af3-110">ก่อนที่คุณจะสามารถเริ่มต้นการใช้งานอีคอมเมิร์ซ คุณต้องเริ่มต้นโครงการ สภาพแวดล้อม และ Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="00af3-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="00af3-111">เมื่อต้องการทำการเริ่มต้นใน LCS คุณต้องได้รับอนุญาตสำหรับบทบาทของเจ้าของโครงการ หรือผู้จัดการสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="00af3-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="00af3-112">รองรับโทโพโลยีสภาพแวดล้อมการผลิตและ Sandbox</span><span class="sxs-lookup"><span data-stu-id="00af3-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="00af3-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)</span><span class="sxs-lookup"><span data-stu-id="00af3-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="00af3-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCSU ให้ดูที่ [เริ่มต้น Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)</span><span class="sxs-lookup"><span data-stu-id="00af3-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="00af3-115">ตั้งค่าเพื่อเริ่มต้นใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="00af3-115">Initialize e-Commerce</span></span>

<span data-ttu-id="00af3-116">ใช้ขั้นตอนต่อไปนี้เพื่อเตรียมใช้งานลักษณะการทำงานอีคอมเมิร์ซในสภาพแวดล้อมที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="00af3-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="00af3-117">ก่อนที่คุณจะเริ่มต้นโปรดตรวจสอบให้แน่ใจว่าคุณมีข้อมูลที่จำเป็นดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="00af3-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="00af3-118">RCSU ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="00af3-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="00af3-119">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับ admins ของระบบอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="00af3-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="00af3-120">กลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory ที่จะใช้สำหรับผู้ดูแลระบบการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="00af3-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="00af3-121">โดเมนที่จะเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="00af3-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="00af3-122">นอกจากนี้คุณยังสามารถรวบรวมข้อมูลเสริมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="00af3-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="00af3-123">Azure AD ข้อมูลธุรกิจ-ผู้บริโภค (B2C):</span><span class="sxs-lookup"><span data-stu-id="00af3-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="00af3-124">ชื่อผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="00af3-124">Tenant Name.</span></span>
    - <span data-ttu-id="00af3-125">รหัสไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="00af3-125">Client ID.</span></span>
    - <span data-ttu-id="00af3-126">โดเมนที่กำหนดเองสำหรับล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="00af3-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="00af3-127">ตอบ URL</span><span class="sxs-lookup"><span data-stu-id="00af3-127">Reply URL.</span></span>
    - <span data-ttu-id="00af3-128">รหัสนโยบายการลงทะเบียนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="00af3-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="00af3-129">รหัสนโยบายการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="00af3-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="00af3-130">แก้ไขรหัสนโยบายโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="00af3-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="00af3-131">คุณสามารถเพิ่มข้อมูลนี้ในภายหลังได้ โดยใช้คำขอบริการ</span><span class="sxs-lookup"><span data-stu-id="00af3-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="00af3-132">หลังจากที่คุณรวบรวมข้อมูลที่จำเป็นแล้ว ให้ทำตามขั้นตอนต่อไปนี้เพื่อเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="00af3-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="00af3-133">ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="00af3-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="00af3-134">เปิดโครงการที่มีสภาพแวดล้อมที่คุณต้องการเตรียมใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="00af3-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="00af3-135">ในส่วนของ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="00af3-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="00af3-136">ภายใต้ **ลักษณะการของสภาพแวดล้อม** เลือกลิงก์ **การจัดการ Retail**</span><span class="sxs-lookup"><span data-stu-id="00af3-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="00af3-137">บนแท็บ **อีคอมเมิร์ซ** ให้เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="00af3-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="00af3-138">กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณต้องป้อนข้อมูลที่จำเป็นสำหรับการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="00af3-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="00af3-139">กรอกข้อมูลที่จำเป็นแล้วไปที่หน้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="00af3-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="00af3-140">บนหน้าถัดไป กรอกข้อมูลที่จำเป็นแล้วกดปุ่มยืนยันฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="00af3-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="00af3-141">คุณกลับไปที่แท็บ **อีคอมเมิร์ซ** ซึ่งคุณควรเห็นการเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="00af3-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="00af3-142">เมื่อต้องการดูสถานะการเริ่มต้น ให้ **รีเฟรช** หรือย้อนกลับไปที่แท็บ **อีคอมเมิร์ซ** ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="00af3-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="00af3-143">เมื่อมีการเริ่มต้นอีคอมเมิร์ซจาก LCS ระบบจะกล่าวถึงส่วนประกอบต่างๆที่จำเป็นสำหรับอีคอมเมิร์ซและเชื่อมโยงกับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="00af3-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="00af3-144">หลังจากการเตรียมใช้งานเสร็จเรียบร้อยแล้ว แท็บ **อีคอมเมิร์ซ** บน **การจัดการขายปลีก** จะถูกอัพเดตเพื่อให้สะท้อนถึงการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="00af3-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="00af3-145">หน้าแสดงการปรับใช้การกำหนดเองล่าสุด และสถานะของการปรับใช้ที่กำลังทำงานอยู่อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="00af3-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="00af3-146">นอกจากนี้ยังมีลิงก์ไปยังไซต์อีคอมเมิร์ซ และเครื่องมือการจัดการไซต์อีคอมเมิร์ซ (เครื่องมือการสร้าง)</span><span class="sxs-lookup"><span data-stu-id="00af3-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="00af3-147">ได้รับสิทธิ์ในการเข้าถึงสภาพแวดล้อมการสร้าง</span><span class="sxs-lookup"><span data-stu-id="00af3-147">Access the authoring environment</span></span>

<span data-ttu-id="00af3-148">ถ้าต้องการเข้าถึงสภาพแวดล้อมการสร้าง ให้ไปที่แท็บ **อีคอมเมิร์ซ** บนหน้า **การจัดการการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="00af3-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="00af3-149">คุณจะพบลิงก์ไปยังไซต์อีคอมเมิร์ซของคุณ และเครื่องมือการจัดการไซต์</span><span class="sxs-lookup"><span data-stu-id="00af3-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00af3-150">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="00af3-150">Additional resources</span></span>

[<span data-ttu-id="00af3-151">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="00af3-151">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="00af3-152">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="00af3-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="00af3-153">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="00af3-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="00af3-154">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="00af3-154">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="00af3-155">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="00af3-155">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="00af3-156">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="00af3-156">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="00af3-157">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="00af3-157">Enable location-based store detection</span></span>](enable-store-detection.md)
