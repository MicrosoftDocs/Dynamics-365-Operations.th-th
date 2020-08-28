---
title: ตั้งค่าผู้เช่า B2C ใน Commerce
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าผู้เช่าของธุรกิจ-ผู้บริโภค (B2C) ของ Azure Active Directory (Azure AD) ของคุณสำหรับการตรวจสอบความถูกต้องของไซต์ของผู้ใช้ใน Dynamics 365 Commerce
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: f31f8898358626f2b008826aa69694dc16742aa0
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677915"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="8e0ef-103">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e0ef-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าผู้เช่าของธุรกิจ-ผู้บริโภค (B2C) ของ Azure Active Directory (Azure AD) ของคุณสำหรับการตรวจสอบความถูกต้องของไซต์ของผู้ใช้ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8e0ef-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-105">Overview</span></span>

<span data-ttu-id="8e0ef-106">Dynamics 365 Commerce ใช้ Azure AD B2C เพื่อสนับสนุนข้อมูลประจำตัวของผู้ใช้และขั้นตอนการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="8e0ef-107">ผู้ใช้สามารถลงชื่อสมัคร ลงชื่อเข้าใช้ และรีเซ็ตรหัสผ่านของพวกเขาได้ผ่านขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="8e0ef-108">Azure AD B2C จัดเก็บข้อมูลการตรวจสอบความถูกต้องของผู้ใช้ที่สำคัญ เช่น ชื่อผู้ใช้ และรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="8e0ef-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="8e0ef-109">เรกคอร์ดผู้ใช้ในผู้เช่าของ B2C จะจัดเก็บเรกคอร์ดบัญชีเฉพาะที่ของ B2C หรือเรกคอร์ดผู้ให้บริการข้อมูลเฉพาะตัวทางสังคมของ B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="8e0ef-110">เรกคอร์ด B2C เหล่านี้จะเชื่อมโยงกลับไปยังเรกคอร์ดลูกค้าในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="8e0ef-111">สร้างหรือเชื่อมโยงกับผู้เช่า B2C ของ AAD ที่มีอยู่ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="8e0ef-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="8e0ef-112">ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="8e0ef-113">จากเมนูของพอร์ทัล Azure เลือก **สร้างทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="8e0ef-114">ตรวจสอบให้แน่ใจว่าได้ใช้การบอกรับเป็นสมาชิกและไดเรกทอรีที่จะเชื่อมต่อกับสภาพแวดล้อม Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![สร้างทรัพยากรในพอร์ทัล Azure](./media/B2CImage_1.png)

1. <span data-ttu-id="8e0ef-116">ไปที่ **ข้อมูลประจำตัว \> Azure Active Directory B2C**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="8e0ef-117">เมื่อหน้า **สร้างผู้เช่า B2C ใหม่ หรือลิงค์ไปยังผู้เช่าที่มีอยู่** ให้ใช้ตัวเลือกใดตัวเลือกหนึ่งด้านล่างที่เหมาะสมกับความต้องการของบริษัทของคุณที่สุด:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="8e0ef-118">**สร้างผู้เช่า Azure AD B2C ใหม่**: ใช้ตัวเลือกนี้เพื่อสร้างผู้เช่า B2C ของ AAD ใหม่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="8e0ef-119">เลือก **สร้างผู้เช่า B2C ของ Azure AD ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="8e0ef-120">ภายใต้ **ชื่อองค์กร** ให้ป้อนชื่อองค์กร</span><span class="sxs-lookup"><span data-stu-id="8e0ef-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="8e0ef-121">ภายใต้ **ชื่อโดเมนเริ่มต้น** ให้ป้อนชื่อโดเมนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8e0ef-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="8e0ef-122">สำหรับ **ประเทศหรือภูมิภาค** ให้เลือกประเทศหรือภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="8e0ef-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="8e0ef-123">เลือก **สร้าง** เพื่อสร้างผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="8e0ef-123">Select **Create** to create the tenant.</span></span>

     ![สร้างผู้เช่า Azure AD ใหม่](./media/B2CImage_2.png)

     - <span data-ttu-id="8e0ef-125">**ลิงค์ผู้เช่าของ Azure AD B2C ที่มีอยู่ไปยังการบอกรับเป็นสมาชิก Azure ของฉัน**: ให้ใช้ตัวเลือกนี้ ถ้าคุณมีผู้เช่าของ Azure AD B2C ที่คุณต้องการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="8e0ef-126">เลือก **ลิงค์ผู้เช่าของ Azure AD B2C ที่มีอยู่ไปยังการบอกรับเป็นสมาชิก Azure ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="8e0ef-127">สำหรับ **ผู้เช่าของ Azure AD B2C** เลือกผู้เช่า B2C ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="8e0ef-128">ถ้าข้อความ "ไม่พบผู้เช่า B2C ที่มีสิทธิ์" ปรากฏขึ้นในกล่องการเลือก คุณจะไม่มีผู้เช่า B2C ที่มีสิทธิ์ที่มีอยู่ และจะต้องสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="8e0ef-129">สำหรับ **กลุ่มทรัพยากร** ให้เลือก **สร้างใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="8e0ef-130">ป้อน **ชื่อ** สำหรับกลุ่มทรัพยากรที่จะมีผู้เช่า เลือก **สถานที่ของกลุ่มทรัพยากร** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![ลิงค์ผู้เช่าของ Azure AD B2C ที่มีอยู่ไปยังการบอกรับเป็นสมาชิก Azure](./media/B2CImage_3.png)

1. <span data-ttu-id="8e0ef-132">หลังจากที่มีการสร้างไดเรกทอรี Azure AD B2C ใหม่ (นี่อาจใช้เวลาสักครู่) ลิงค์ไปยังไดเรกทอรีใหม่จะปรากฏขึ้นบนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8e0ef-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="8e0ef-133">ลิงค์นี้จะนำคุณไปยังหน้า "ยินดีต้อนรับสู่ Azure Active Directory B2C"</span><span class="sxs-lookup"><span data-stu-id="8e0ef-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![ลิงค์ไปยังไดเรกทอรี AAD ใหม่](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="8e0ef-135">ถ้าคุณมีการบอกรับเป็นสมาชิกหลายรายภายในบัญชี Azure ของคุณ หรือตั้งค่าผู้เช่า B2C โดยไม่มีการเชื่อมโยงกับการบอกรับเป็นสมาชิกที่ใช้งานอยู่ แบนเนอร์ **แก้ไขปัญหา** จะนำคุณไปลิงค์ผู้เช่ากับการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="8e0ef-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="8e0ef-136">เลือกข้อความการแก้ไขปัญหา และทำตามคำแนะนำเพื่อแก้ไขปัญหาการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="8e0ef-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="8e0ef-137">รูปภาพต่อไปนี้แสดงตัวอย่างของแบนเนอร์ **การแก้ไขปัญหา** ของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![คำเตือนที่แสดงไดเรกทอรีไม่มีการบอกรับเป็นสมาชิกที่ใช้งานอยู่](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="8e0ef-139">สร้างแอพลิเคชัน B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-139">Create the B2C application</span></span>

<span data-ttu-id="8e0ef-140">เมื่อมีการสร้างผู้เช่า B2C คุณจะสร้างแอพลิเคชัน B2C ภายในผู้เช่าเพื่อโต้ตอบกับการดำเนินการ Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="8e0ef-141">เมื่อต้องการสร้างแอพลิเคชัน B2C ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-142">ในพอร์ทัล Azure เลือก **แอปพลิเคชัน (ดั้งเดิม)** แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-142">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="8e0ef-143">ภายใต้ **ชื่อ** ให้ป้อนชื่อของแอพลิเคชัน B2C ของ AAD ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="8e0ef-144">ภายใต้ **เว็บแอป/Web API** สำหรับ **รวมเว็บแอป / API เว็บ** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="8e0ef-145">สำหรับ **อนุญาตขั้นตอนโดยนัย** เลือก **ใช่** (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="8e0ef-146">ภายใต้ **ตอบ URL** ให้ป้อน URL ตอบกลับที่จัดสรรไว้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="8e0ef-147">โปรดดูที่ [ตอบ URL](#reply-urls) ด้านล่าง สำหรับข้อมูลเกี่ยวกับ URL ตอบกลับและวิธีจัดรูปแบบไฟล์เหล่านั้นที่นี่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="8e0ef-148">สำหรับ **รวมไคลเอนต์ดั้งเดิม** เลือก **ไม่** (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="8e0ef-149">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="8e0ef-150">ตอบกลับ URLs</span><span class="sxs-lookup"><span data-stu-id="8e0ef-150">Reply URLs</span></span>

<span data-ttu-id="8e0ef-151">การตอบกลับ URLs มีความสำคัญ เนื่องจากมีการอนุญาตรายการของโดเมนส่งคืน เมื่อไซต์ของคุณเรียกใช้ Azure AD B2C เพื่อตรวจสอบความถูกต้องของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="8e0ef-152">การอนุญาตนี้จะช่วยให้การส่งคืนของผู้ใช้ที่ได้รับการรับรองความถูกต้องสามารถกลับไปยังโดเมนที่มีการลงชื่อเข้าใช้ (โดเมนของไซต์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="8e0ef-153">ในกล่อง **ตอบกลับ URL** บนหน้าจอ **Azure AD B2c - แอพลิเคชัน \> แอพลิเคชันใหม่** คุณต้องเพิ่มรายการที่แยกต่างหากสำหรับทั้งโดเมนไซต์ของคุณและ (เมื่อมีการเตรียมใช้งานสภาพแวดล้อมของคุณ) URL ที่สร้างโดย Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="8e0ef-154">URL เหล่านี้ต้องใช้รูปแบบ URL ที่ถูกต้องเสมอ และต้องเป็น URL พื้นฐานเท่านั้น (ไม่มีเครื่องหมายสแลชหรือพาธต่อท้าย)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="8e0ef-155">จากนั้น สตริง ``/_msdyn365/authresp`` ต้องถูกผนวกเข้ากับ URL พื้นฐาน ตามตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="8e0ef-156">``https://www.fabrikam.com/_msdyn365/authresp`` (โดเมนควรตรงกับโดเมนอีคอมเมิร์ซทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8e0ef-156">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="8e0ef-157">ถ้าคุณมีหลายโดเมน คุณต้องเพิ่ม URL นี้สำหรับแต่ละโดเมน)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-157">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="8e0ef-158">สร้างนโยบายขั้นตอนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-158">Create user flow policies</span></span>

<span data-ttu-id="8e0ef-159">ขั้นตอนของผู้ใช้เป็นนโยบายที่ Azure AD B2C ใช้เพื่อให้ประสบการณ์การใช้งานของผู้ใช้ในการลงชื่อเข้าใช้ ลงชื่อสมัคร แก้ไขโพรไฟล์ และลืมรหัสผ่าน ที่มีความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-159">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="8e0ef-160">Dynamics 365 Commerce ใช้ขั้นตอนเหล่านี้เพื่อดำเนินการกับนโยบายเพื่อโต้ตอบกับผู้เช่าของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-160">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="8e0ef-161">เมื่อผู้ใช้โต้ตอบกับนโยบายเหล่านี้ จะมีการเปลี่ยนเส้นทางไปยังผู้เช่าของ Azure AD B2C เพื่อทำการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-161">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="8e0ef-162">Azure AD B2C มีชนิดขั้นตอนของผู้ใช้พื้นฐานสามชนิดดังนี้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-162">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="8e0ef-163">ลงชื่อสมัครใช้และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-163">Sign up and sign in</span></span>
- <span data-ttu-id="8e0ef-164">การแก้ไขโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="8e0ef-164">Profile editing</span></span>
- <span data-ttu-id="8e0ef-165">รีเซ็ตรหัสผ่านแล้ว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-165">Password reset</span></span>

<span data-ttu-id="8e0ef-166">คุณสามารถเลือกที่จะใช้ขั้นตอนของผู้ใช้เริ่มต้นที่ระบุโดย Azure AD ซึ่งจะแสดงหน้าที่โฮสต์โดย AAD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-166">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="8e0ef-167">อีกทางหนึ่งคือ คุณสามารถสร้างหน้า HTML เพื่อควบคุมรูปลักษณ์และความรู้สึกของประสบการณ์ขั้นตอนของผู้ใช้เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-167">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="8e0ef-168">เมื่อต้องการกำหนดหน้านโยบายผู้ใช้สำหรับ Dynamics 365 Commerce ให้ดูที่ [ตั้งค่าหน้าแบบกำหนดเองสำหรับล็อกอินของผู้ใช้](custom-pages-user-logins.md)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-168">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="8e0ef-169">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [กำหนดค่าอินเทอร์เฟสของประสบการณ์การใช้งานของผู้ใช้ใน Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-169">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="8e0ef-170">การสร้างนโยบายขั้นตอนของผู้ใช้ในการลงชื่อสมัครและการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-170">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="8e0ef-171">เมื่อต้องการสร้างนโยบายขั้นตอนของผู้ใช้ในการลงชื่อสมัครและการลงชื่อเข้าใช้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-171">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-172">ในพอร์ทัล Azure เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)** ในบานหน้าต่างนำทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-172">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="8e0ef-173">ในหน้า **Azure AD B2C – ขั้นตอนของผู้ใช้ (นโยบาย)** เลือก **ขั้นตอนของผู้ใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-173">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="8e0ef-174">บนแท็บ **แนะนำ** ให้เลือก **ลงชื่อสมัครใช้และลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-174">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="8e0ef-175">ภายใต้ **ชื่อ** ให้ป้อนชื่อนโยบาย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-175">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="8e0ef-176">ชื่อนี้จะแสดงขึ้นหลังจากที่มีคำนำหน้าที่พอร์ทัลกำหนด (ตัวอย่างเช่น "B2C_1_")</span><span class="sxs-lookup"><span data-stu-id="8e0ef-176">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="8e0ef-177">ภายใต้ **ผู้ให้บริการข้อมูลเฉพาะตัว** เลือกกล่องกาเครื่องหมายที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-177">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="8e0ef-178">ภายใต้ **การตรวจสอบความถูกต้องของ Multifactor** เลือกตัวเลือกที่เหมาะสมสำหรับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-178">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="8e0ef-179">ภายใต้ **แอททริบิวต์และการอ้างสิทธิ์ของผู้ใช้** เลือกตัวเลือกเพื่อรวบรวมแอททริบิวต์หรือส่งคืนการอ้างสิทธิ์ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-179">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="8e0ef-180">Commerce ต้องมีตัวเลือกเริ่มต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-180">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="8e0ef-181">**รวบรวมแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-181">**Collect  attribute**</span></span> | <span data-ttu-id="8e0ef-182">**การอ้างสิทธิ์การส่งคืนสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-182">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="8e0ef-183">ที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="8e0ef-183">Email Address</span></span>          | <span data-ttu-id="8e0ef-184">ที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="8e0ef-184">Email Addresses</span></span>   |
    | <span data-ttu-id="8e0ef-185">ชื่อที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="8e0ef-185">Given Name</span></span>             | <span data-ttu-id="8e0ef-186">ชื่อที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="8e0ef-186">Given Name</span></span>        |
    |                        | <span data-ttu-id="8e0ef-187">ตัวให้บริการข้อมูลเฉพาะตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-187">Identity Provider</span></span> |
    | <span data-ttu-id="8e0ef-188">นามสกุล</span><span class="sxs-lookup"><span data-stu-id="8e0ef-188">Surname</span></span>                | <span data-ttu-id="8e0ef-189">นามสกุล</span><span class="sxs-lookup"><span data-stu-id="8e0ef-189">Surname</span></span>           |
    |                        | <span data-ttu-id="8e0ef-190">รหัสออบเจ็กต์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-190">User’s Object ID</span></span>  |

1. <span data-ttu-id="8e0ef-191">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-191">Select **Create**.</span></span>

<span data-ttu-id="8e0ef-192">รูปภาพต่อไปนี้เป็นตัวอย่างของการลงชื่อเข้าใช้ของ Azure AD B2C และขั้นตอนของผู้ใช้ในการลงทะเบียนและการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-192">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![การตั้งค่านโยบายในการลงทะเบียนและการลงชื่อเข้าใช้](./media/B2CImage_11.png)

<span data-ttu-id="8e0ef-194">รูปภาพต่อไปนี้แสดงตัวเลือก **รันขั้นตอนของผู้ใช้** ในขั้นตอนของผู้ใช้ในการลงทะเบียนและการลงชื่อเข้าใช้ของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-194">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![รันตัวเลือกขั้นตอนของผู้ใช้ในขั้นตอนของนโยบาย](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="8e0ef-196">สร้างนโยบายขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="8e0ef-196">Create a profile editing user flow policy</span></span>

<span data-ttu-id="8e0ef-197">เมื่อต้องการสร้างนโยบายขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-197">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-198">ในพอร์ทัล Azure เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)** ในบานหน้าต่างนำทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-198">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="8e0ef-199">ในหน้า **Azure AD B2C – ขั้นตอนของผู้ใช้ (นโยบาย)** เลือก **ขั้นตอนของผู้ใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-199">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="8e0ef-200">บนแท็บ **แนะนำ** ให้เลือก **การแก้ไขโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-200">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="8e0ef-201">ภายใต้ **ชื่อ** ให้ป้อนขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="8e0ef-201">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="8e0ef-202">ชื่อนี้จะแสดงขึ้นหลังจากที่มีคำนำหน้าที่พอร์ทัลกำหนด (ตัวอย่างเช่น "B2C_1_")</span><span class="sxs-lookup"><span data-stu-id="8e0ef-202">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="8e0ef-203">ภายใต้ **ตัวให้บริการข้อมูลเฉพาะตัว** ให้เลือก **ลงชื่อเข้าใช้บัญชีท้องถิ่น**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-203">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="8e0ef-204">ภายใต้ **แอททริบิวต์ของผู้ใช้** เลือกกล่องกาเครื่องหมายใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-204">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="8e0ef-205">**ที่อยู่อีเมล** (**การอ้างสิทธิ์การส่งคืนสินค้า** เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-205">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="8e0ef-206">**ชื่อที่กำหนด** (**รวบรวมแอททริบิวต์** และ **การอ้างสิทธิ์การส่งคืนสินค้า**)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-206">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="8e0ef-207">**ตัวให้บริการข้อมูลเฉพาะตัว** (**การอ้างสิทธิ์การส่งคืนสินค้า** เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-207">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="8e0ef-208">**นามสกุล** (**รวบรวมแอททริบิวต์** และ **การอ้างสิทธิ์การส่งคืนสินค้า**)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-208">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="8e0ef-209">**รหัสออบเจ็กต์ของผู้ใช้** (**การอ้างสิทธิ์การส่งคืนสินค้า** เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-209">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="8e0ef-210">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-210">Select **Create**.</span></span>

<span data-ttu-id="8e0ef-211">รูปภาพต่อไปนี้แสดงตัวอย่างของขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-211">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![สร้างนโยบายของผู้ใช้ในการแก้ไขโพรไฟล์](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="8e0ef-213">สร้างนโยบายขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="8e0ef-213">Create a password reset user flow policy</span></span>

<span data-ttu-id="8e0ef-214">เมื่อต้องการสร้างนโยบายขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่าน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-214">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-215">ในพอร์ทัล Azure เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)** ในบานหน้าต่างนำทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-215">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="8e0ef-216">ในหน้า **Azure AD B2C – ขั้นตอนของผู้ใช้ (นโยบาย)** เลือก **ขั้นตอนของผู้ใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-216">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="8e0ef-217">บนแท็บ **แนะนำ** ให้เลือก **การรีเซ็ตรหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-217">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="8e0ef-218">ภายใต้ **ชื่อ** ให้ป้อนชื่อสำหรับขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="8e0ef-218">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="8e0ef-219">ภายใต้ **ตัวให้บริการข้อมูลเฉพาะ** เลือก **รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-219">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="8e0ef-220">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-220">Select **Create**.</span></span>
1. <span data-ttu-id="8e0ef-221">ภายใต้ **การเรียกร้องสิทธิ์ในแอปพลิเคชัน** เลือกกล่องกาเครื่องหมายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-221">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="8e0ef-222">**ที่อยู่อีเมล**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-222">**Email addresses**</span></span>
    - <span data-ttu-id="8e0ef-223">**ชื่อที่กำหนด**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-223">**Given Name**</span></span>
    - <span data-ttu-id="8e0ef-224">**นามสกุล**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-224">**Surname**</span></span>
    - <span data-ttu-id="8e0ef-225">**รหัสออบเจ็กต์ของผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-225">**User's Object ID**</span></span>
1. <span data-ttu-id="8e0ef-226">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-226">Select **Create**.</span></span>

<span data-ttu-id="8e0ef-227">รูปภาพต่อไปนี้แสดงตำแหน่งที่จะตั้งค่า **รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล** ในขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่านของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-227">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![ตั้งค่า "รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล" ในนโยบายการรีเซ็ตรหัสผ่าน](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="8e0ef-229">เพิ่มผู้ให้บริการข้อมูลประจำตัวทางสังคม (เลือกกำหนดได้)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-229">Add social identity providers (Optional)</span></span>

<span data-ttu-id="8e0ef-230">ผู้ให้บริการข้อมูลประจำตัวทางสังคมอนุญาตให้ผู้ใช้สามารถใช้บัญชีทางสังคมของตนเพื่อตรวจสอบความถูกต้องได้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-230">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="8e0ef-231">ไม่จำเป็นต้องระบุการเพิ่มการรับรองความถูกต้องของผู้ให้บริการข้อมูลประจำตัวทางสังคมใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-231">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="8e0ef-232">ถ้าไม่มีการเพิ่มการตรวจสอบความถูกต้องของผู้ให้บริการข้อมูลประจำตัวทางสังคม โพรไฟล์ของ Azure AD B2C เริ่มต้นจะเป็นโพรไฟล์หลักสำหรับฐานผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-232">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="8e0ef-233">ผู้ใช้จะเลือกชื่อผู้ใช้ของตนเอง (ที่อยู่อีเมลที่ต้องการของพวกเขา) และตั้งค่ารหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="8e0ef-233">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="8e0ef-234">Azure AD B2C จะตรวจสอบความถูกต้องผู้ใช้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-234">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="8e0ef-235">ถ้ามีการเพิ่มการตรวจสอบความถูกต้องของผู้ให้บริการข้อมูลประจำตัวทางสังคม และผู้ใช้เลือกหนึ่งในผู้ให้บริการข้อมูลประจำตัวทางสังคมที่เสนอ จะยังคงมีการสร้างเอนทิตีในผู้เช่าของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-235">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="8e0ef-236">Azure AD B2C จะตรวจสอบความถูกต้องของข้อมูลประจำตัวของผู้ใช้ที่มีผู้ให้บริการข้อมูลประจำตัวทางสังคม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-236">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="8e0ef-237">การลงชื่อเข้าใช้ของตัวให้บริการข้อมูลเฉพาะตัวจะสร้างเรกคอร์ดในผู้เช่า B2C แต่อยู่ในรูปแบบที่แตกต่างจากบัญชีภายในเครื่อง เนื่องจากจะเรียกข้อมูลอ้างอิงของผู้ให้บริการข้อมูลประจำตัวทางสังคมภายนอกสำหรับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-237">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="8e0ef-238">ผู้ใช้สามารถใช้ที่อยู่อีเมลเดียวกันในผู้ให้บริการข้อมูลประจำตัวทางสังคมต่างๆ ซึ่งหมายความว่าชื่อผู้ใช้อีเมลที่ใช้สำหรับการรับรองความถูกต้องอาจไม่ซ้ำกันกับผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="8e0ef-238">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="8e0ef-239">Azure AD B2C จะบังคับใช้เฉพาะผู้ใช้ที่มีที่อยู่อีเมลที่ไม่ซ้ำกันบนบัญชี B2C เฉพาะที่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8e0ef-239">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="8e0ef-240">ก่อนที่คุณจะสามารถเพิ่มผู้ให้บริการข้อมูลประจำตัวของสังคมสำหรับการรับรองความถูกต้องได้ คุณต้องไปที่เว็บไซต์ของผู้ให้บริการข้อมูลประจำตัวและตั้งค่าแอปพลิเคชันตัวให้บริการข้อมูลเฉพาะตัวตามคำสั่งในเอกสารของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-240">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="8e0ef-241">มีรายการของลิงค์ไปยังเอกสารด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-241">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="8e0ef-242">Amazon</span><span class="sxs-lookup"><span data-stu-id="8e0ef-242">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="8e0ef-243">Azure AD (ผู้เช่าเดียว)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-243">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="8e0ef-244">บัญชี Microsoft</span><span class="sxs-lookup"><span data-stu-id="8e0ef-244">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="8e0ef-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="8e0ef-245">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="8e0ef-246">GitHub</span><span class="sxs-lookup"><span data-stu-id="8e0ef-246">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="8e0ef-247">Google</span><span class="sxs-lookup"><span data-stu-id="8e0ef-247">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="8e0ef-248">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="8e0ef-248">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="8e0ef-249">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="8e0ef-249">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="8e0ef-250">Twitter</span><span class="sxs-lookup"><span data-stu-id="8e0ef-250">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="8e0ef-251">เพิ่มและตั้งค่าผู้ให้บริการข้อมูลประจำตัวทางสังคม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-251">Add and set up a social identity provider</span></span>

<span data-ttu-id="8e0ef-252">เมื่อต้องการเพิ่มและตั้งค่าผู้ให้บริการข้อมูลประจำตัวทางสังคม ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-252">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="8e0ef-253">ในพอร์ทัล Azure ให้นำทางไปยัง **ผู้ให้บริการข้อมูลประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-253">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="8e0ef-254">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-254">Select **Add**.</span></span> <span data-ttu-id="8e0ef-255">หน้าจอ **เพิ่มผู้ให้บริการข้อมูลประจำตัว** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e0ef-255">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="8e0ef-256">ภายใต้ **ชื่อ** ให้ป้อนชื่อที่จะแสดงให้กับผู้ใช้บนหน้าจอลงชื่อเข้าใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-256">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="8e0ef-257">ภายใต้ **ชนิดผู้ให้บริการข้อมูลประจำตัว** เลือกผู้ให้บริการข้อมูลประจำตัวจากรายการ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-257">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="8e0ef-258">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-258">Select **OK**.</span></span>
1. <span data-ttu-id="8e0ef-259">เลือก **ตั้งค่าผู้ให้บริการข้อมูลประจำตัวนี้** เพื่อเข้าถึงหน้าจอ **ตั้งค่าผู้ให้บริการข้อมูลประจำตัวทางสังคม**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-259">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="8e0ef-260">ภายใต้ **รหัสไคลเอนต์** ให้ป้อนรหัสไคลเอนต์ที่ได้รับมาจากการตั้งค่าแอปพลิเคชันของผู้ให้บริการข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-260">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="8e0ef-261">ภายใต้ **ข้อมูลลับไคลเอนต์** ให้ป้อนข้อมูลลับไคลเอนต์ที่ได้รับมาจากการตั้งค่าแอปพลิเคชันของผู้ให้บริการข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-261">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="8e0ef-262">แนบขั้นตอนของผู้ใช้สำหรับนโยบายการลงชื่อเข้าใช้และการลงชื่อสมัครใช้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-262">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="8e0ef-263">ไปที่ **Azure AD B2C – ขั้นตอนผู้ใช้ (นโยบาย) \> {นโยบายการลงชื่อเข้าใช้และการลงชื่อสมัครใช้ของคุณ} \> ผู้ให้บริการข้อมูลประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-263">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="8e0ef-264">เมื่อต้องการแนบนโยบายขั้นตอนการลงชื่อเข้าใช้/การลงชื่อสมัครใช้ ให้เลือกผู้ให้บริการข้อมูลประจำตัวแต่ละรายการที่คุณตั้งค่าไว้สำหรับบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-264">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="8e0ef-265">เมื่อต้องการทดสอบรายการเหล่านี้ ให้เลือก **รันขั้นตอนของผู้ใช้** สำหรับผู้ให้บริการข้อมูลประจำตัวแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-265">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="8e0ef-266">แท็บใหม่จะแสดงหน้าการลงชื่อเข้าใช้ซึ่งแสดงกล่องการเลือกผู้ให้บริการข้อมูลประจำตัวใหม่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-266">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="8e0ef-267">รูปภาพต่อไปนี้แสดงตัวอย่างของ **เพิ่มผู้ให้บริการข้อมูลประจำตัว** และหน้าจอ **ตั้งค่าผู้ให้บริการข้อมูลประจำตัวทางสังคม** ใน Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-267">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![การเพิ่มผู้ให้บริการข้อมูลประจำตัวทางสังคมไปยังแอพลิเคชันของคุณ](./media/B2CImage_14.png)

<span data-ttu-id="8e0ef-269">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการเลือกผู้ให้บริการข้อมูลประจำตัวในหน้า **ผู้ให้บริการข้อมูลประจำตัว** ของ Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-269">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![เลือกผู้ให้บริการข้อมูลประจำตัวทางสังคมแต่ละรายการเพื่อเปิดใช้งานสำหรับนโยบายของคุณ](./media/B2CImage_16.png)

<span data-ttu-id="8e0ef-271">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้าจอการลงชื่อเข้าใช้เริ่มต้นที่มีปุ่มการลงชื่อเข้าใช้ของผู้ให้บริการข้อมูลประจำตัวทางสังคมที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-271">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![ตัวอย่างหน้าจอล็อกอินเริ่มต้นที่มีปุ่มการลงชื่อเข้าใช้ของผู้ให้บริการข้อมูลประจำตัวทางสังคมที่แสดงอยู่](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="8e0ef-273">อัพเดตศูนย์ควบคุม Commerce ด้วยข้อมูล Azure AD B2C ใหม่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-273">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="8e0ef-274">เมื่อมีขั้นตอนการเตรียมใช้งาน Azure AD B2C ด้านบนเสร็จเรียบร้อยแล้ว แอพลิเคชัน Azure AD B2C ต้องมีการลงทะเบียนในสภาพแวดล้อม Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-274">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="8e0ef-275">เมื่อต้องการปรับปรุงศูนย์ควบคุมด้วยข้อมูล Azure AD B2C ใหม่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-275">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-276">ใน Commerce ให้ไปที่ **พารามิเตอร์ที่ใช้ร่วมกันของ Commerce** และเลือก **ผู้ให้บริการข้อมูลเฉพาะตัว** ในเมนูด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-276">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="8e0ef-277">ภายใต้ **ผู้ให้บริการข้อมูลเฉพาะตัว** ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-277">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="8e0ef-278">ในกล่อง **ผู้ออก** ให้ป้อน URL ผู้ออกของผู้ให้บริการข้อมูลเฉพาะตัว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-278">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="8e0ef-279">ในการค้นหา URL ของผู้ออกของคุณ โปรดดูที่ [รับ URL ของผู้ออก](#obtain-issuer-url) ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-279">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="8e0ef-280">ในกล่อง **ชื่อ** ให้ป้อนชื่อสำหรับเรกคอร์ดผู้ออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-280">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="8e0ef-281">ในกล่อง **ชนิด** ให้ป้อน **Azure AD B2C (id_token)**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-281">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="8e0ef-282">ภายใต้ **บริษัทที่เกี่ยวข้อง** ที่มีรายการของผู้ให้บริการข้อมูลเฉพาะตัวของ B2C ที่เลือก ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e0ef-282">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="8e0ef-283">ในกล่อง **รหัสไคลแอนต์** ให้ป้อนรหัสแอพลิเคชัน B2C ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-283">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="8e0ef-284">คุณสามารถค้นหาข้อมูลนี้ได้ในกล่อง **รหัสแอพลิเคชัน** ของหน้าคุณสมบัติของแอพลิเคชัน B2C ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-284">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="8e0ef-285">ในกล่อง **ชนิด** ให้ป้อน **สาธารณะ**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-285">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="8e0ef-286">ในกล่อง **ชนิดผู้ใช้** ให้ป้อน **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-286">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="8e0ef-287">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-287">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="8e0ef-288">ในกล่องค้นหา Commerce ให้ค้นหา **กำหนดการการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-288">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="8e0ef-289">ในเมนูนำทางด้านซ้ายของหน้า **กำหนดการการกระจาย** ให้เลือกงาน **1110 การตั้งค่าคอนฟิกส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-289">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="8e0ef-290">บนบานหน้าต่างการดำเนินการ เลือก **รันตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-290">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="8e0ef-291">รับ URL ของผู้ออก</span><span class="sxs-lookup"><span data-stu-id="8e0ef-291">Obtain issuer URL</span></span>

<span data-ttu-id="8e0ef-292">เมื่อต้องการได้รับ URL ผู้ออกของผู้ให้บริการข้อมูลเฉพาะตัวของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-292">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-293">สร้าง URL ที่อยู่ข้อมูลเมตาในรูปแบบต่อไปนี้โดยใช้ผู้เช่า B2C และนโยบายของคุณ: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="8e0ef-293">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="8e0ef-294">ตัวอย่าง: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``</span><span class="sxs-lookup"><span data-stu-id="8e0ef-294">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="8e0ef-295">ป้อน URL ที่อยู่ของข้อมูลเมตาลงในแถบที่อยู่ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="8e0ef-295">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="8e0ef-296">ในข้อมูลเมตา คัดลอก URL ผู้ออกของผู้ให้บริการข้อมูลประจำตัว (ค่าสำหรับ **"ผู้ออก"**)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-296">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="8e0ef-297">ตัวอย่าง: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``</span><span class="sxs-lookup"><span data-stu-id="8e0ef-297">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="8e0ef-298">ตั้งค่าคอนฟิกผู้เช่า B2C ของคุณในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-298">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="8e0ef-299">เมื่อการตั้งค่าของผู้เช่า Azure AD B2C ของคุณเสร็จสมบูรณ์แล้ว คุณต้องตั้งค่าคอนฟิกผู้เช่า B2c ในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-299">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="8e0ef-300">ขั้นตอนการตั้งค่าคอนฟิกรวมถึงการรวบรวมข้อมูลแอพลิเคชัน B2C จากพอร์ทัล Azure การป้อนข้อมูลแอพลิเคชัน B2C ลงในโปรแกรมสร้างไซต์ และจากนั้น เชื่อมโยงแอพลิเคชัน B2C กับไซต์และช่องทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-300">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="8e0ef-301">รวบรวมข้อมูลแอพลิเคชันที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8e0ef-301">Collect the required application information</span></span>

<span data-ttu-id="8e0ef-302">เมื่อต้องการรวบรวมข้อมูลแอพลิเคชันที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-302">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-303">ในพอร์ทัล Azure ให้ไปที่ **หน้าหลัก \> Azure AD B2C - แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-303">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="8e0ef-304">เลือกแอพลิเคชันของคุณ และจากนั้น ในบานหน้าต่างนำทางด้านซ้าย เลือก **คุณสมบัติ** เพื่อดูรายละเอียดแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8e0ef-304">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="8e0ef-305">จากกล่อง **รหัสแอพลิเคชัน** ให้รวบรวมรหัสแอพลิเคชันของแอพลิเคชัน B2C ที่สร้างขึ้นในผู้เช่า B2C ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-305">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="8e0ef-306">นี่จะถูกป้อนเป็น **GUID ของไคลเอนต์** ในโปรแกรมสร้างไซต์ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-306">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="8e0ef-307">ภายใต้ **ตอบกลับ URL** ให้รวบรวมการตอบกลับ URL</span><span class="sxs-lookup"><span data-stu-id="8e0ef-307">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="8e0ef-308">ไปที่ **หน้าหลัก \> Azure AD B2C – ขั้นตอนผู้ใช้ (นโยบาย)** แล้วรวบรวมชื่อของนโยบายขั้นตอนของผู้ใช้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-308">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="8e0ef-309">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้า **Azure AD B2C - แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-309">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![นำทางไปยังแอพลิเคชัน B2C ภายในผู้เช่าของคุณ](./media/B2CImage_19.png)

<span data-ttu-id="8e0ef-311">รูปภาพต่อไปนี้แสดงตัวอย่างของหน้า **คุณสมบัติ** ของแอพลิเคชันใน Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-311">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![คัดลอกรหัสของแอพลิเคชันจากคุณสมบัติของแอพลิเคชัน B2C](./media/B2CImage_21.png)

<span data-ttu-id="8e0ef-313">รูปภาพต่อไปนี้แสดงตัวอย่างของนโยบายขั้นตอนของผู้ใช้ในหน้า **Azure AD B2C – ขั้นตอนผู้ใช้ (นโยบาย)**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-313">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![รวบรวมชื่อของขั้นตอนของนโยบาย B2C แต่ละรายการ](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="8e0ef-315">ป้อนข้อมูลแอพลิเคชันของผู้เช่า AAD B2C ของคุณลงใน Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-315">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="8e0ef-316">คุณต้องป้อนรายละเอียดของผู้เช่า Azure AD ผู้เช่า ลงในโปรแกรมสร้างไซต์ Commerce ก่อนที่จะเชื่อมโยงผู้เช่า B2C กับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-316">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="8e0ef-317">เมื่อต้องการเพิ่มข้อมูลแอพลิเคชันของผู้เช่า AAD B2C ลงใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-317">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-318">ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบในโปรแกรมสร้างไซต์ Commerce สำหรับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-318">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="8e0ef-319">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-319">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="8e0ef-320">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **การตั้งค่า B2C**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-320">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="8e0ef-321">ในหน้าต่างหลักถัดจาก **แอพลิเคชัน B2C** เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-321">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="8e0ef-322">(ถ้าผู้เช่าของคุณปรากฎในรายการแอพลิเคชัน B2C แสดงว่ามีการเพิ่มโดยผู้ดูแลระบบแล้ว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-322">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="8e0ef-323">ตรวจสอบว่าสินค้าในขั้นตอนที่ 6 ข้างล่างนี้ตรงกับแอพลิเคชัน B2C ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-323">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="8e0ef-324">เลือก **เพิ่มแอพลิเคชัน B2C**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-324">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="8e0ef-325">ป้อนรายการที่จำเป็นต่อไปนี้ในฟอร์มที่แสดง โดยใช้ค่าจากผู้เช่า B2C และแอพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-325">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="8e0ef-326">ฟิลด์ที่ไม่จำเป็น (ฟิลด์ที่ไม่มีเครื่องหมายดอกจัน) อาจถูกปล่อยว่างไว้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-326">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="8e0ef-327">**ชื่อแอพลิเคชัน**: ชื่อสำหรับแอพลิเคชัน B2C ของคุณ ตัวอย่างเช่น "Fabrikam B2C"</span><span class="sxs-lookup"><span data-stu-id="8e0ef-327">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="8e0ef-328">**ชื่อผู้เช่า**: ชื่อของผู้เช่า B2C ของคุณ (ตัวอย่างเช่น ใช้ "fabrikam" ถ้าโดเมนปรากฏเป็น "fabrikam.onmicrosoft.com" สำหรับผู้เช่า B2C)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-328">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="8e0ef-329">**รหัสนโยบายของการลืมรหัสผ่าน**: รหัสนโยบายของขั้นตอนผู้ใช้ในการลืมรหัสผ่าน ตัวอย่างเช่น "B2C_1_PasswordReset"</span><span class="sxs-lookup"><span data-stu-id="8e0ef-329">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="8e0ef-330">**รหัสนโยบายของการลงทะเบียนและการลงชื่อเข้าใช้** รหัสนโยบายของขั้นตอนผู้ใช้ในการลงทะเบียนและการลงชื่อเข้าใช้ ตัวอย่างเช่น "B2C_1_signup_signin"</span><span class="sxs-lookup"><span data-stu-id="8e0ef-330">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="8e0ef-331">**GUID ของไคลเอนต์**: รหัสแอพลิเคชัน B2C ตัวอย่างเช่น "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6"</span><span class="sxs-lookup"><span data-stu-id="8e0ef-331">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="8e0ef-332">**รหัสนโยบายของการแก้ไขโพรไฟล์**: รหัสนโยบายของขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ ตัวอย่างเช่น "B2C_1A_ProfileEdit"</span><span class="sxs-lookup"><span data-stu-id="8e0ef-332">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="8e0ef-333">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-333">Select **OK**.</span></span> <span data-ttu-id="8e0ef-334">ขณะนี้คุณควรดูชื่อของแอพลิเคชัน B2C ของคุณที่ปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-334">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="8e0ef-335">เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-335">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="8e0ef-336">เชื่อมโยงแอพลิเคชัน B2C กับไซต์และช่องทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="8e0ef-337">ถ้าไซต์ของคุณเชื่อมโยงกับแอพลิเคชัน B2C อยู่แล้ว การเปลี่ยนไปยังแอพลิเคชัน B2C อื่นจะลบการอ้างอิงปัจจุบันที่สร้างขึ้นสำหรับผู้ใช้ที่ลงชื่อสมัครในสภาพแวดล้อมนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8e0ef-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="8e0ef-338">ถ้ามีการเปลี่ยนแปลง ข้อมูลประจำตัวใดๆ ที่เชื่อมโยงกับแอพลิเคชัน B2C ที่กำหนดไว้ในปัจจุบันจะไม่พร้อมใช้งานสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="8e0ef-339">ปรับปรุงเฉพาะแอพลิเคชัน B2C ถ้าคุณกำลังตั้งค่าแอพลิเคชัน B2C ของช่องทางเป็นครั้งแรก หรือถ้าคุณต้องการให้ผู้ใช้ลงชื่อสมัครใหม่โดยใช้ข้อมูลประจำตัวใหม่ไปยังช่องทางนี้กับแอพลิเคชัน B2C ใหม่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="8e0ef-340">ใช้ความระมัดระวังเมื่อเชื่อมโยงช่องทางไปยังแอพลิเคชัน B2C และมีการระบุชื่อแอพลิเคชันอย่างชัดแจ้ง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="8e0ef-341">ถ้าช่องทางไม่เชื่อมโยงกับแอพลิเคชัน B2C ในขั้นตอนด้านล่าง ผู้ใช้ที่ลงชื่อเข้าใช้ในช่องทางดังกล่าวสำหรับไซต์ของคุณจะถูกป้อนลงในแอพลิเคชัน B2C ที่แสดงเป็น **ค่าเริ่มต้น** ในรายการ **การตั้งค่าผู้เช่า \> การตั้งค่า B2C** ของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8e0ef-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="8e0ef-342">เพื่อเชื่อมโยงแอพลิเคชัน B2C กับไซต์และช่องทางของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="8e0ef-343">นำทางไปยังไซต์ของคุณในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="8e0ef-344">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="8e0ef-345">ด้านล่าง **การตั้งค่าไซต์** เลือก **ช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="8e0ef-346">ในหน้าต่างหลักภายใต้ **ช่องทาง** เลือกช่องทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="8e0ef-347">ในบานหน้าต่างคุณสมบัติช่องทางทางด้านขวา ให้เลือกชื่อแอพลิเคชัน B2C ของคุณจากเมนูแบบหล่นลงของ **เลือกแอพลิเคชัน B2C**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="8e0ef-348">เลือก **ปิด** แล้วเลือก **บันทึกและเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="8e0ef-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="8e0ef-349">ข้อมูล B2C เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="8e0ef-350">การโยกย้ายลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8e0ef-350">Customer migration</span></span>

<span data-ttu-id="8e0ef-351">ถ้าคุณกำลังพิจารณาการย้ายเรกคอร์ดลูกค้าจากแพลตฟอร์มของผู้ให้บริการข้อมูลประจำตัวก่อนหน้า โปรดทำงานกับทีม Dynamics 365 Commerce เพื่อตรวจสอบความต้องการการโยกย้ายลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="8e0ef-352">สำหรับเอกสาร Azure AD B2C เพิ่มเติมสำหรับการโยกย้ายลูกค้า โปรดดู [โยกย้ายผู้ใช้ไปยัง Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration)การ B2C</span><span class="sxs-lookup"><span data-stu-id="8e0ef-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="8e0ef-353">นโยบายที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-353">Custom policies</span></span>

<span data-ttu-id="8e0ef-354">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการปรับแต่งการโต้ตอบ Azure AD B2C และขั้นตอนนโยบายนอกเหนือจากที่มีนำเสนอโดยนโยบายมาตรฐานของ B2C โปรดดู [นโยบายที่กำหนดเองใน Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="8e0ef-355">ผู้ดูแลระบบรอง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-355">Secondary admin</span></span>

<span data-ttu-id="8e0ef-356">คุณสามารถเพิ่มบัญชีผู้ดูแลระบบรองหรือไม่ก็ได้ในส่วน **ผู้ใช้** ของผู้เช่า B2C ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="8e0ef-357">นี่อาจเป็นบัญชีโดยตรงหรือบัญชีทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8e0ef-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="8e0ef-358">ถ้าคุณต้องการแบ่งปันบัญชีระหว่างทรัพยากรทีมร่วมกัน ยังสามารถสร้างบัญชีทั่วไปได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8e0ef-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="8e0ef-359">เนื่องจากความสำคัญของข้อมูลที่จัดเก็บไว้ใน Azure AD B2C ควรมีการตรวจสอบความถูกต้องของบัญชีทั่วไปอย่างใกล้ชิดตามแนวทางปฏิบัติด้านความปลอดภัยของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e0ef-360">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8e0ef-360">Additional resources</span></span>

[<span data-ttu-id="8e0ef-361">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8e0ef-362">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="8e0ef-362">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8e0ef-363">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="8e0ef-363">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8e0ef-364">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-364">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8e0ef-365">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="8e0ef-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8e0ef-366">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="8e0ef-366">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8e0ef-367">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8e0ef-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8e0ef-368">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="8e0ef-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8e0ef-369">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="8e0ef-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8e0ef-370">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8e0ef-370">Enable location-based store detection</span></span>](enable-store-detection.md)
