---
title: เตรียมใช้งานสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426476"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="95401-103">เตรียมใช้งานสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="95401-104">หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="95401-105">ก่อนที่คุณจะเริ่มต้น เราขอแนะนำให้คุณอ่านผ่านหัวข้อนี้เพื่อดูว่ากระบวนการต้องใช้อะไร</span><span class="sxs-lookup"><span data-stu-id="95401-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="95401-106">ถ้าคุณยังไม่ได้รับอนุญาตให้เข้าถึงการแสดงตัวอย่างของ Dynamics 365 Commerce คุณสามารถร้องขอการเข้าถึงการแสดงตัวอย่างได้จาก [เว็บไซต์  Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)</span><span class="sxs-lookup"><span data-stu-id="95401-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="95401-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="95401-107">Overview</span></span>

<span data-ttu-id="95401-108">เพื่อเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณให้สำเร็จ คุณต้องสร้างโครงการที่มีชื่อและชนิดของผลิตภัณฑ์ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="95401-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="95401-109">สภาพแวดล้อมและ Commerce Scale Unit (CSU) ก็มีพารามิเตอร์เฉพาะบางอย่างที่คุณต้องใช้เมื่อคุณเตรียมใช้งานอีคอมเมิร์ซในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="95401-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="95401-110">คำแนะนำในหัวข้อนี้อธิบายขั้นตอนที่จำเป็นทั้งหมดที่คุณต้องทำการเตรียมใช้งานให้เสร็จสมบูรณ์ และพารามิเตอร์ที่คุณต้องใช้</span><span class="sxs-lookup"><span data-stu-id="95401-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="95401-111">หลังจากที่คุณเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณเสร็จสิ้น คุณต้องดำเนินการขั้นตอนหลังการเตรียมใช้งานสองสามขั้นตอนเพื่อจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="95401-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="95401-112">ขั้นตอนบางอย่างอาจไม่จำเป็น ขึ้นอยู่กับแง่มุมของระบบที่คุณต้องการประเมิน</span><span class="sxs-lookup"><span data-stu-id="95401-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="95401-113">คุณสามารถดำเนินการตามขั้นตอนที่ไม่จำเป็นในภายหลังได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="95401-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="95401-114">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ หลังจากที่คุณเตรียมใช้งาน ให้ดูที่ [ตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](cpe-post-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="95401-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="95401-115">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ หลังจากที่คุณเตรียมใช้งาน ให้ดูที่ [ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](cpe-optional-features.md)</span><span class="sxs-lookup"><span data-stu-id="95401-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="95401-116">หากคุณมีคำถามใดๆ เกี่ยวกับขั้นตอนการเตรียมใช้งาน หรือหากคุณพบปัญหาใดๆ โปรดแจ้งให้ Microsoft ทราบใน [กลุ่ม Microsoft Dynamics 365 Commerce Preview Yammer](https://aka.ms/Dynamics365CommercePreviewYammer)</span><span class="sxs-lookup"><span data-stu-id="95401-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="95401-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="95401-117">Prerequisites</span></span>

<span data-ttu-id="95401-118">ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้ก่อนที่คุณจะสามารถเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณได้:</span><span class="sxs-lookup"><span data-stu-id="95401-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="95401-119">คุณมีสิทธิ์เข้าถึงพอร์ทัล Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="95401-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="95401-120">คุณเป็นคู่ค้าหรือลูกค้า Microsoft Dynamics 365 แล้ว และสามารถสร้างโครงการ Dynamics 365 Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="95401-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="95401-121">คุณได้รับการยอมรับในโปรแกรม Dynamics 365 Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="95401-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="95401-122">คุณมีสิทธิ์ที่จำเป็นในการสร้างโครงการสำหรับ **โยกย้าย สร้างวิธีแก้ไข และเรียนรู้**</span><span class="sxs-lookup"><span data-stu-id="95401-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="95401-123">คุณเป็นส่วนหนึ่งของบทบาท **ผู้จัดการสภาพแวดล้อม** หรือ **เจ้าของโครงการ** ในโครงการที่คุณจะเตรียมใช้งานสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="95401-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="95401-124">คุณมีสิทธิ์เข้าถึงในฐานะผู้ดูแลระบบสำหรับการสมัครใช้งาน Microsoft Azure ของคุณ หรือคุณมีการติดต่อกับผู้ดูแลระบบการสมัครใช้งานที่สามารถดำเนินการขั้นตอนสองขั้นตอนที่ต้องการสิทธิ์ของผู้ดูแลระบบในนามของคุณให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="95401-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="95401-125">คุณมีรหัสผู้เช่า Azure Active Directory (Azure AD) ของคุณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="95401-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="95401-126">คุณได้สร้างกลุ่มรักษาความปลอดภัย Azure AD ที่สามารถใช้เป็นกลุ่มผู้ดูแลระบบอีคอมเมิร์ซ และคุณมีรหัสที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="95401-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="95401-127">คุณได้สร้างกลุ่มรักษาความปลอดภัย Azure AD ที่สามารถใช้เป็นกลุ่มผู้ดูแลการให้คะแนนและบทวิจารณ์ และคุณมีรหัสที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="95401-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="95401-128">(กลุ่มความปลอดภัยนี้อาจเหมือนกับกลุ่มผู้ดูแลระบบพาณิชย์อิเล็กทรอนิกส์)</span><span class="sxs-lookup"><span data-stu-id="95401-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="95401-129">เตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="95401-130">กระบวนงานเหล่านี้จะอธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="95401-131">หลังจากที่คุณดำเนินการเสร็จสมบูรณ์แล้ว สภาพแวดล้อมของการแสดงตัวอย่างของ Commerce จะพร้อมสำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="95401-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="95401-132">กิจกรรมทั้งหมดที่อธิบายไว้ที่นี่จะเกิดขึ้นในพอร์ทัล LCS</span><span class="sxs-lookup"><span data-stu-id="95401-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95401-133">การเข้าถึงการแสดงตัวอย่างจะเชื่อมโยงกับบัญชี LCS และองค์กรที่คุณระบุไว้ในแอพลิเคชันการแสดงตัวอย่าง Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="95401-134">คุณต้องใช้บัญชีเดียวกันเพื่อเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="95401-135">ถ้าคุณต้องใช้บัญชี LCS หรือผู้เช่าที่แตกต่างกันสำหรับสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce คุณต้องให้รายละเอียดเหล่านั้นไปยัง Microsoft</span><span class="sxs-lookup"><span data-stu-id="95401-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="95401-136">สำหรับข้อมูลผู้ติดต่อ โปรดดูส่วน [การสนับสนุนสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](#commerce-preview-environment-support) ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="95401-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="95401-137">ยืนยันว่าคุณลักษณะการแสดงตัวอย่างพร้อมใช้งานและถูกเปิดใช้งานใน LCS</span><span class="sxs-lookup"><span data-stu-id="95401-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="95401-138">เพื่อยืนยันว่าคุณลักษณะการแสดงตัวอย่างพร้อมใช้งานและถูกเปิดใช้งานใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="95401-139">ลงชื่อเข้าใช้ [พอร์ทัล LCS](https://lcs.dynamics.com) โดยใช้บัญชี LCS เดียวกันกับที่คุณใช้ในการร้องขอการเข้าถึงไปยังการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="95401-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="95401-140">ในโฮมเพจของ LCS ให้เลื่อนไปทางขวาสุด และเลือกไทล์ **การจัดการคุณลักษณะการแสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="95401-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![ดูตัวอย่างไทล์การจัดการ](./media/preview1.png)

1. <span data-ttu-id="95401-142">เลื่อนลงไปที่ **คุณลักษณะการแสดงตัวอย่างส่วนตัว** และยืนยันว่าคุณลักษณะต่อไปนี้พร้อมใช้งานและถูกเปิดใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="95401-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="95401-143">การประเมินอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="95401-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="95401-144">สภาพแวดล้อมของโปรแกรมตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-144">Commerce Preview Program Environments</span></span>

    ![คุณลักษณะแสดงตัวอย่างแบบส่วนตัว](./media/preview2.png)

1. <span data-ttu-id="95401-146">ถ้าคุณลักษณะเหล่านั้นไม่ปรากฏในรายการ โปรดติดต่อ Microsoft และระบุที่อยู่อีเมลที่ทำงานของคุณ บัญชี LCS และรายละเอียดผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="95401-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="95401-147">สำหรับข้อมูลผู้ติดต่อ โปรดดูส่วน [การสนับสนุนสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](#commerce-preview-environment-support)</span><span class="sxs-lookup"><span data-stu-id="95401-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="95401-148">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="95401-148">Create a new project</span></span>

<span data-ttu-id="95401-149">เมื่อต้องการสร้างโครงการใหม่ใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="95401-150">บนโฮมเพจ LCS ให้เลือกเครื่องหมายบวก (**+**) เพื่อสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="95401-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="95401-151">ในบานหน้าต่างด้านขวา ให้ทำตามหนึ่งในขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="95401-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="95401-152">ถ้าคุณเป็นคู่ค้า ให้เลือก **โยกย้าย สร้างวิธีแก้ไข และเรียนรู้**</span><span class="sxs-lookup"><span data-stu-id="95401-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="95401-153">ถ้าคุณเป็นลูกค้า ให้เลือก **การเปิดจำหน่ายล่วงหน้าสำหรับผู้ที่มีแนวโน้มจะเป็นลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="95401-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="95401-154">ป้อนชื่อ คำอธิบาย และอุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="95401-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="95401-155">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้เลือก **Dynamics 365 Retail**</span><span class="sxs-lookup"><span data-stu-id="95401-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="95401-156">ในฟิลด์ **รุ่นผลิตภัณฑ์** ให้เลือก **Dynamics 365 Retail**</span><span class="sxs-lookup"><span data-stu-id="95401-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="95401-157">ในฟิลด์ **วิธีการ** ให้เลือก **วิธีการใช้งานการขายปลีกของ Dynamics**</span><span class="sxs-lookup"><span data-stu-id="95401-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="95401-158">ไม่จำเป็นต้องระบุ: คุณสามารถนำเข้าบทบาทและผู้ใช้จากโครงการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="95401-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="95401-159">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="95401-159">Select **Create**.</span></span> <span data-ttu-id="95401-160">มุมมองโครงการจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="95401-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="95401-161">เพิ่มตัวเชื่อมต่อ Azure</span><span class="sxs-lookup"><span data-stu-id="95401-161">Add the Azure Connector</span></span>

<span data-ttu-id="95401-162">ในการเพิ่มตัวเชื่อมต่อ Azure ไปยังโครงการ LCS ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="95401-163">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="95401-164">หากคุณเป็นคู่ค้า ให้เลือกไทล์ **การตั้งค่าโครงการ** ที่ด้านขวาสุด</span><span class="sxs-lookup"><span data-stu-id="95401-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="95401-165">ถ้าคุณเป็นลูกค้า ให้เลือก **การตั้งค่าโครงการ** บนเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="95401-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="95401-166">เลือก **ตัวเชื่อมต่อ Azure**</span><span class="sxs-lookup"><span data-stu-id="95401-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="95401-167">เลือก **เพิ่ม** เพื่อเพิ่มตัวเชื่อมต่อ Azure</span><span class="sxs-lookup"><span data-stu-id="95401-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="95401-168">ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="95401-168">Enter a name.</span></span>
1. <span data-ttu-id="95401-169">ป้อนรหัสการสมัครใช้งาน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="95401-170">เปิดใช้งานตัวเลือก **ตั้งค่าคอนฟิกเพื่อใช้ Azure Resource Manager (ARM)**</span><span class="sxs-lookup"><span data-stu-id="95401-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="95401-171">ตรวจสอบว่าค่า **โดเมน (หรือรหัส) ผู้เช่า AAD ในการสมัครใช้งาน Azure AAD** ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="95401-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="95401-172">โปรดปรึกษาผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="95401-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="95401-173">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="95401-173">Select **Next**.</span></span>
1. <span data-ttu-id="95401-174">ทำตามคำแนะนำบนหน้าเพื่อให้สิทธิ์การเข้าถึงแอพลิเคชันที่จำเป็นแก่การสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="95401-175">โปรดปรึกษาผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="95401-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="95401-176">ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="95401-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="95401-177">ตรวจสอบให้แน่ใจว่าได้เลือกไดเรกทอรีที่ถูกต้อง และจากนั้น บนเมนูทางซ้ายให้เลือก **การสมัครใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="95401-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="95401-178">ค้นหาการสมัครเข้าใช้งานที่ถูกต้องในรายการ แล้วเลือกรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="95401-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="95401-179">ใช้ฟังก์ชันการค้นหาตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="95401-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="95401-180">บนเมนู เลือก **การควบคุมการเข้าถึง (IAM)**</span><span class="sxs-lookup"><span data-stu-id="95401-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="95401-181">ทางด้านขวา ภายใต้ **เพิ่มการกำหนดบทบาท** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="95401-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="95401-182">บานหน้าต่าง **เพิ่มการกำหนดบทบาท** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="95401-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="95401-183">ในฟิลด์ **บทบาท** ให้เลือก **ผู้สนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="95401-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="95401-184">ในฟิลด์ **กำหนดการเข้าถึงไปยัง** ให้ละทิ้งค่าเริ่มต้น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**</span><span class="sxs-lookup"><span data-stu-id="95401-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="95401-185">ภายใต้ **เลือก** ให้ป้อน **b96b7e94-b82e-4e71-99a0-cf7fb188acea**</span><span class="sxs-lookup"><span data-stu-id="95401-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="95401-186">เลือก **Dynamics Deployment Services \[wsfed-enabled\]** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="95401-187">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="95401-187">Select **Save**.</span></span>

1. <span data-ttu-id="95401-188">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="95401-188">Select **Next**.</span></span>
1. <span data-ttu-id="95401-189">ทำตามคำแนะนำบนหน้าเพื่อให้สิทธิ์การเข้าถึงแอพลิเคชันที่จำเป็นแก่การสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="95401-190">โปรดปรึกษาผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="95401-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="95401-191">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="95401-191">Select **Next**.</span></span>
1. <span data-ttu-id="95401-192">ในฟิลด์ **ภูมิภาคของ Azure** เลือก **สหรัฐอเมริกาตะวันออก** **สหรัฐอเมริกาตะวันออก 2** **สหรัฐอเมริกาตะวันตก** หรือ **สหรัฐอเมริกาตะวันตก 2**</span><span class="sxs-lookup"><span data-stu-id="95401-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="95401-193">เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="95401-193">Select **Connect**.</span></span> <span data-ttu-id="95401-194">ตัวเชื่อมต่อ Azure ของคุณน่าจะปรากฏขึ้นในรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="95401-195">นำเข้าส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="95401-196">ถ้าต้องการนำเข้าส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce ลงในโครงการของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="95401-197">เปิดโฮมเพจสำหรับโครงการของคุณโดยการเลือกชื่อโครงการที่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="95401-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="95401-198">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="95401-199">หากคุณเป็นคู่ค้า ให้เลือกไทล์ **ไลบรารีแอสเซท** ที่ด้านขวาสุด</span><span class="sxs-lookup"><span data-stu-id="95401-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="95401-200">ถ้าคุณเป็นลูกค้า ให้เลือก **ไลบรารีแอสเซท** บนเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="95401-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="95401-201">ในรายการทางด้านซ้าย เลือก **แพคเกจที่สามารถปรับใช้ได้ของซอฟต์แวร์**</span><span class="sxs-lookup"><span data-stu-id="95401-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="95401-202">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="95401-202">Select **Import**.</span></span>
1. <span data-ttu-id="95401-203">ภายใต้ **ไลบรารีแอสเซทที่ใช้ร่วมกัน** เลือก **ส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce** ในรายการของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="95401-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="95401-204">เลือก **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="95401-204">Select **Pick**.</span></span> <span data-ttu-id="95401-205">คุณถูกส่งกลับไปยังไลบรารีแอสเซท และคุณควรเห็นส่วนขยายในรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="95401-206">ภาพประกอบต่อไปนี้แสดงการดำเนินการที่ต้องดำเนินการบนหน้า **ไลบรารีแอสเซท** ของ LCS</span><span class="sxs-lookup"><span data-stu-id="95401-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![การนำเข้าส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="95401-208">ปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="95401-208">Deploy the environment</span></span>

<span data-ttu-id="95401-209">เพื่อปรับใช้สภาพแวดล้อม ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="95401-210">คุณอาจไม่จำเป็นต้องทำตามขั้นตอนที่ 6 7 และ/หรือ 8 ให้เสร็จสมบูรณ์ เนื่องจากเพจที่มีตัวเลือกเดียวจะถูกข้ามไป</span><span class="sxs-lookup"><span data-stu-id="95401-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="95401-211">เมื่อคุณอยู่ในมุมมอง **พารามิเตอร์สภาพแวดล้อม** ให้ยืนยันว่าข้อความ **Dynamics 365 Commerce - สาธิต (10.0.* x* ที่มีการอัพเดตแพลตฟอร์ม *xx*)\*\* จะปรากฏขึ้นเหนือฟิลด์ **ชื่อสภาพแวดล้อม** โดยตรง</span><span class="sxs-lookup"><span data-stu-id="95401-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="95401-212">สำหรับรายละเอียด ให้ดูภาพประกอบที่ปรากฏหลังจากขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="95401-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="95401-213">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="95401-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="95401-214">เลือก **เพิ่ม** เพื่อเพิ่มสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="95401-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="95401-215">ในฟิลด์ **รุ่นของแอพลิเคชัน** ให้เลือกเวอร์ชันที่เป็นปัจจุบันมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="95401-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="95401-216">ถ้าคุณต้องเลือกรุ่นของแอพลิเคชันอื่นที่ไม่ใช่เวอร์ชันที่เป็นปัจจุบันมากที่สุด อย่าเลือกรุ่นก่อนหน้ารุ่น **10.0.8**</span><span class="sxs-lookup"><span data-stu-id="95401-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="95401-217">ในฟิลด์ **เวอร์ชันของแพลตฟอร์ม** ให้ใช้เวอร์ชันของแพลตฟอร์มที่เลือกโดยอัตโนมัติสำหรับเวอร์ชันของแอพลิเคชันที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="95401-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![การเลือกรุ่นของแอพลิเคชันและแพลตฟอร์ม](./media/project1.png)

1. <span data-ttu-id="95401-219">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="95401-219">Select **Next**.</span></span>
1. <span data-ttu-id="95401-220">เลือก **สาธิต** เป็นโทโพโลยีสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="95401-220">Select **Demo** as the environment topology.</span></span>

    ![การเลือกโทโพโลยีสภาพแวดล้อม 1](./media/project2.png)

1. <span data-ttu-id="95401-222">เลือก **Dynamics 365 Commerce - สาธิต** เป็นโทโพโลยีสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="95401-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="95401-223">ถ้าคุณได้ตั้งค่าคอนฟิกตัวเชื่อมต่อ Azure แบบเดี่ยวก่อนหน้านี้แล้ว จะมีการใช้สำหรับสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="95401-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="95401-224">ถ้าคุณตั้งค่าคอนฟิกตัวเชื่อมต่อ Azure ที่หลากหลาย คุณสามารถเลือกตัวเชื่อมต่อที่จะใช้: **สหรัฐอเมริกาตะวันออก** **สหรัฐอเมริกาตะวันออก 2** **สหรัฐอเมริกาตะวันตก 2** หรือ **สหรัฐอเมริกาตะวันตก 2**</span><span class="sxs-lookup"><span data-stu-id="95401-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="95401-225">สำหรับประสิทธิภาพการทำงานแบบครอบคลุมที่ดีที่สุด เราขอแนะนำให้คุณเลือก **สหรัฐอเมริกาตะวันตก 2**)</span><span class="sxs-lookup"><span data-stu-id="95401-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![การเลือกโทโพโลยีสภาพแวดล้อม 2](./media/project3.png)

1. <span data-ttu-id="95401-227">บนเพจ **ปรับใช้สภาพแวดล้อม** ให้ป้อนชื่อสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="95401-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="95401-228">ปล่อยการตั้งค่าขั้นสูงไว้ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="95401-228">Leave the advanced settings as they are.</span></span>

    ![ปรับใช้เพจสภาพแวดล้อม](./media/project4.png)

1. <span data-ttu-id="95401-230">ปรับขนาด VM ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="95401-230">Adjust the VM size as required.</span></span> <span data-ttu-id="95401-231">(เราขอแนะนำหน่วยการเก็บสต็อกสินค้า VM \[SKU\] **D13 v2**)</span><span class="sxs-lookup"><span data-stu-id="95401-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="95401-232">ตรวจสอบเงื่อนไขการกำหนดราคาและการให้สิทธิ์การใช้งาน และจากนั้น เลือกกล่องกาเครื่องหมายเพื่อบ่งชี้ว่าคุณเห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="95401-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="95401-233">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="95401-233">Select **Next**.</span></span>
1. <span data-ttu-id="95401-234">บนหน้ายืนยันการปรับใช้ ตรวจสอบว่ารายละเอียดทั้งหลายถูกต้อง และจากนั้น เลือก **ปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="95401-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="95401-235">คุณจะกลับไปยังมุมมอง **สภาพแวดล้อมที่ใช้ Cloud** และสภาพแวดล้อมของคุณควรจะปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="95401-236">สภาพแวดล้อมที่ร้องขอของคุณจะปรากฎเป็นอยู่ในคิว และจากนั้นจะเปลี่ยนเป็นกำลังปรับใช้</span><span class="sxs-lookup"><span data-stu-id="95401-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="95401-237">เวิร์กโฟลว์สภาพแวดล้อมจะใช้เวลาสักครู่เพื่อให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="95401-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="95401-238">ดังนั้น โปรดกลับมาตรวจสอบหลังจากประมาณหกถึงเก้าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="95401-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="95401-239">ก่อนที่คุณจะดำเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าสถานะของสภาพแวดล้อมของคุณคือ **ปรับใช้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="95401-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="95401-240">เริ่มต้น Commerce Scale Unit (ระบบคลาวด์)</span><span class="sxs-lookup"><span data-stu-id="95401-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="95401-241">เมื่อต้องการเริ่มต้น CSU ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="95401-242">ในมุมมอง **สภาพแวดล้อมที่ใช้ Cloud** ให้เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="95401-243">ในมุมมองสภาพแวดล้อมทางด้านขวา เลือก **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="95401-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="95401-244">มุมมองรายละเอียดของสภาพแวดล้อมจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="95401-244">The environment details view appears.</span></span>
1. <span data-ttu-id="95401-245">ภายใต้ **คุณลักษณะของสภาพแวดล้อม** ให้เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="95401-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="95401-246">บนแท็บ **Commerce** ให้เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="95401-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="95401-247">มุมมองพารามิเตอร์สำหรับการเริ่มต้นใช้งาน CSU จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="95401-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="95401-248">ในฟิลด์ **ภูมิภาค** เลือก **สหรัฐอเมริกาตะวันออก** **สหรัฐอเมริกาตะวันออก 2** **สหรัฐอเมริกาตะวันตก** หรือ **สหรัฐอเมริกาตะวันตก 2**</span><span class="sxs-lookup"><span data-stu-id="95401-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="95401-249">ในฟิลด์ **รุ่น** ให้เลือก **ระบุรุ่น** ในรายการ และจากนั้น ระบุ **9.18.20014.4** ในฟิลด์ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="95401-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="95401-250">ตรวจสอบให้แน่ใจว่าได้ระบุรุ่นที่แน่นอนซึ่งถูกระบุไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="95401-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="95401-251">มิฉะนั้น คุณจะต้องปรับปรุง RCSU เป็นรุ่นที่ถูกต้องในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="95401-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="95401-252">เปิดใช้งานตัวเลือก **ใช้ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="95401-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="95401-253">ในรายการส่วนขยาย ให้เลือก **ส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="95401-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="95401-254">เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="95401-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="95401-255">บนหน้ายืนยันการปรับใช้ ตรวจสอบว่ารายละเอียดทั้งหลายถูกต้อง และจากนั้น เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="95401-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="95401-256">มุมมอง **การจัดการ Commerce** จะแสดงอีกครั้งโดยที่แท็บ **Commerce** จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="95401-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="95401-257">CSU ของคุณได้รับการจัดคิวสำหรับการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="95401-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="95401-258">ก่อนที่คุณจะดำเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าสถานะของ CSU ของคุณคือ **สำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="95401-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="95401-259">การเริ่มต้นใช้งานจะใช้เวลาประมาณสองถึงห้าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="95401-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="95401-260">ตั้งค่าเพื่อเริ่มต้นใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="95401-260">Initialize e-Commerce</span></span>

<span data-ttu-id="95401-261">เมื่อต้องการเริ่มต้นอีคอมเมิร์ซ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95401-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="95401-262">บนแท็บ **อีคอมเมิร์ซ** ให้ตรวจสอบความยินยอมในการแสดงตัวอย่าง และจากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="95401-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="95401-263">ในฟิลด์ **ชื่อผู้เช่าอีคอมเมิร์ซ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="95401-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="95401-264">อย่างไรก็ตาม โปรดทราบว่าชื่อนี้จะปรากฏในบาง URL ที่ชี้ไปยังอินสแตนซ์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="95401-265">ในฟิลด์ **ชื่อ Commerce Scale Unit** เลือก CSU ของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="95401-266">(รายการควรมีเพียงตัวเลือกเดียว)</span><span class="sxs-lookup"><span data-stu-id="95401-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="95401-267">ฟิลด์ **ภูมิศาสตร์ของอีคอมเมิร์ซ** ถูกตั้งค่าโดยอัตโนมัติ และไม่สามารถเปลี่ยนค่าได้</span><span class="sxs-lookup"><span data-stu-id="95401-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="95401-268">เลือก **ถัดไป** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="95401-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="95401-269">ในฟิลด์ **ชื่อโฮสต์ที่ได้รับการสนับสนุน** ให้ป้อนโดเมนที่ถูกต้องใดๆ เช่น `www.fabrikam.com`</span><span class="sxs-lookup"><span data-stu-id="95401-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="95401-270">ในฟิลด์ **กลุ่มความปลอดภัย AAD สำหรับผู้ดูแลระบบ** ให้ป้อนอักษรสองสามตัวแรกของชื่อของกลุ่มความปลอดภัยที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="95401-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="95401-271">เลือกไอคอนคลาสการขยายเพื่อแสดงผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="95401-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="95401-272">เลือกกลุ่มความปลอดภัยที่ถูกต้องจากรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="95401-273">ในฟิลด์ **กลุ่มความปลอดภัย AAD สำหรับการให้คะแนนและตรวจสอบผู้ตรวจสอบ** ให้ป้อนอักษรสองสามตัวแรกของชื่อของกลุ่มความปลอดภัยที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="95401-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="95401-274">เลือกไอคอนคลาสการขยายเพื่อแสดงผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="95401-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="95401-275">เลือกกลุ่มความปลอดภัยที่ถูกต้องจากรายการ</span><span class="sxs-lookup"><span data-stu-id="95401-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="95401-276">ปล่อยให้ตัวเลือก **เปิดใช้งานบริการการให้คะแนนและบทวิจารณ์** เปิด</span><span class="sxs-lookup"><span data-stu-id="95401-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="95401-277">เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="95401-277">Select **Initialize**.</span></span> <span data-ttu-id="95401-278">มุมมอง **การจัดการ Commerce** จะแสดงอีกครั้งโดยที่แท็บ **อีคอมเมิร์ซ** จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="95401-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="95401-279">การเริ่มใช้งานอีคอมเมิร์ซได้เริ่มต้นขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="95401-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="95401-280">ก่อนที่คุณจะดำเนินการต่อไป ให้รอจนกว่าสถานะของการเริ่มต้นใช้งานอีคอมเมิร์ซจะเป็น **การเริ่มต้นใช้งานสำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="95401-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="95401-281">ภายใต้ **ลิงค์** ที่ด้านล่างขวา ให้จดบันทึก URL สำหรับลิงค์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95401-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="95401-282">**ไซต์อีคอมเมิร์ซ** – การเชื่อมโยงไปยังรากของไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="95401-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="95401-283">**เครื่องมือการจัดการไซต์อีคอมเมิร์ซ** – การเชื่อมโยงไปยังเครื่องมือการจัดการไซต์</span><span class="sxs-lookup"><span data-stu-id="95401-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="95401-284">การสนับสนุนสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-284">Commerce preview environment support</span></span>

<span data-ttu-id="95401-285">ถ้าคุณประสบปัญหาขณะที่คุณกำลังดำเนินการขั้นตอนการจัดเตรียมให้เสร็จสมบูรณ์ โปรดเยี่ยมชม [กลุ่ม Microsoft Dynamics 365 Commerce Preview Yammer](https://aka.ms/Dynamics365CommercePreviewYammer) สำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="95401-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="95401-286">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="95401-286">Next steps</span></span>

<span data-ttu-id="95401-287">เพื่อดำเนินการกระบวนการในการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณต่อ ให้ดูที่ [ตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](cpe-post-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="95401-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95401-288">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="95401-288">Additional resources</span></span>

[<span data-ttu-id="95401-289">ภาพรวมของสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="95401-290">ตั้งค่าคอนฟิกสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="95401-291">ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="95401-292">FAQ เกี่ยวกับสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="95401-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="95401-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="95401-294">Commerce Scale Unit (ระบบคลาวด์)</span><span class="sxs-lookup"><span data-stu-id="95401-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="95401-295">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="95401-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="95401-296">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95401-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

