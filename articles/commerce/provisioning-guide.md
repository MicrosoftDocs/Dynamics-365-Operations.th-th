---
title: เตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce
description: หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934759"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="51ca9-103">เตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="51ca9-104">หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="51ca9-105">ก่อนที่คุณจะเริ่ม อย่างน้อยที่สุดเราขอแนะนำให้คุณอ่านหัวข้อทั้งหมดนี้อย่างผ่านๆ เพื่อให้เข้าใจแนวคิดเกี่ยวกับกระบวนการที่เกี่ยวข้องและหัวข้อนี้มีอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="51ca9-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="51ca9-106">ถ้าคุณยังไม่ได้รับอนุญาตให้เข้าถึงการแสดงตัวอย่างของ Dynamics 365 Commerce คุณสามารถร้องขอการเข้าถึงการแสดงตัวอย่างได้จาก [เว็บไซต์ Commerce](https://aka.ms/Dynamics365CommerceWebsite)</span><span class="sxs-lookup"><span data-stu-id="51ca9-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="51ca9-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="51ca9-107">Overview</span></span>

<span data-ttu-id="51ca9-108">เพื่อเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณให้สำเร็จ คุณต้องสร้างโครงการที่มีชื่อและชนิดของผลิตภัณฑ์ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="51ca9-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="51ca9-109">สภาพแวดล้อมและ Retail Cloud Scale Unit (RCSU) ก็มีพารามิเตอร์เฉพาะบางอย่างที่คุณต้องใช้ เมื่อคุณเตรียมใช้งานอีคอมเมิร์ซในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="51ca9-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="51ca9-110">คำแนะนำในหัวข้อนี้อธิบายขั้นตอนที่จำเป็นทั้งหมดที่คุณต้องทำให้เสร็จสมบูรณ์และพารามิเตอร์ที่คุณต้องใช้</span><span class="sxs-lookup"><span data-stu-id="51ca9-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="51ca9-111">หลังจากที่คุณเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณเสร็จสิ้น คุณต้องดำเนินการขั้นตอนหลังการเตรียมใช้งานสองสามขั้นตอนเพื่อจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="51ca9-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="51ca9-112">ขั้นตอนบางอย่างอาจไม่จำเป็น ขึ้นอยู่กับแง่มุมของระบบที่คุณต้องการประเมิน</span><span class="sxs-lookup"><span data-stu-id="51ca9-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="51ca9-113">คุณสามารถดำเนินการตามขั้นตอนที่ไม่จำเป็นในภายหลังได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="51ca9-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="51ca9-114">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ หลังจากที่คุณเตรียมใช้งาน ให้ดูที่ [ตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](cpe-post-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="51ca9-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="51ca9-115">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ หลังจากที่คุณเตรียมใช้งาน ให้ดูที่ [ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](cpe-optional-features.md)</span><span class="sxs-lookup"><span data-stu-id="51ca9-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="51ca9-116">หากคุณมีคำถามใดๆ เกี่ยวกับขั้นตอนการเตรียมใช้งาน หรือหากคุณพบปัญหาใดๆ โปรดแจ้งให้ Microsoft ทราบใน [กลุ่ม Microsoft Dynamics 365 Commerce Preview Yammer](https://aka.ms/Dynamics365CommercePreviewYammer)</span><span class="sxs-lookup"><span data-stu-id="51ca9-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="51ca9-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-117">Prerequisites</span></span>

<span data-ttu-id="51ca9-118">ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้ก่อนที่คุณจะสามารถเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณได้:</span><span class="sxs-lookup"><span data-stu-id="51ca9-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="51ca9-119">คุณมีสิทธิ์เข้าถึงพอร์ทัล Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="51ca9-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="51ca9-120">คุณได้รับการยอมรับในโปรแกรม Dynamics 365 Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="51ca9-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="51ca9-121">คุณมีสิทธิ์ที่จำเป็นในการสร้างโครงการสำหรับ **การเปิดจำหน่ายล่วงหน้าสำหรับผู้ที่มีแนวโน้มจะเป็นลูกค้า** หรือ **โยกย้าย สร้างวิธีแก้ไข และเรียนรู้**</span><span class="sxs-lookup"><span data-stu-id="51ca9-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="51ca9-122">คุณเป็นส่วนหนึ่งของบทบาท **ผู้จัดการสภาพแวดล้อม** หรือ **เจ้าของโครงการ** ในโครงการที่คุณจะเตรียมใช้งานสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="51ca9-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="51ca9-123">คุณมีสิทธิ์เข้าถึงในฐานะผู้ดูแลระบบสำหรับการสมัครใช้งาน Microsoft Azure ของคุณ หรือคุณมีการติดต่อกับผู้ดูแลระบบการสมัครใช้งานที่สามารถดำเนินการขั้นตอนสองขั้นตอนที่ต้องการสิทธิ์ของผู้ดูแลระบบในนามของคุณให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="51ca9-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="51ca9-124">คุณมีรหัสผู้เช่า Azure Active Directory (Azure AD) ของคุณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51ca9-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="51ca9-125">คุณได้สร้างกลุ่มรักษาความปลอดภัย Azure AD ที่สามารถใช้เป็นกลุ่มผู้ดูแลระบบอีคอมเมิร์ซ และคุณมีรหัสที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51ca9-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="51ca9-126">คุณได้สร้างกลุ่มรักษาความปลอดภัย Azure AD ที่สามารถใช้เป็นกลุ่มผู้ดูแลการให้คะแนนและบทวิจารณ์ และคุณมีรหัสที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51ca9-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="51ca9-127">(กลุ่มความปลอดภัยนี้อาจเหมือนกับกลุ่มผู้ดูแลระบบพาณิชย์อิเล็กทรอนิกส์)</span><span class="sxs-lookup"><span data-stu-id="51ca9-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="51ca9-128">ค้นหารหัสผู้เช่า Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="51ca9-129">รหัสผู้เช่า Azure AD ของคุณเป็น Global Unique Identifier (GUID) ที่คล้ายกับตัวอย่างนี้: **72f988bf-86f1-41af-91ab-2d7cd011db47**</span><span class="sxs-lookup"><span data-stu-id="51ca9-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="51ca9-130">ค้นหารหัสผู้เช่า Azure AD ของคุณโดยใช้พอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="51ca9-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="51ca9-131">ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="51ca9-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="51ca9-132">ตรวจสอบให้แน่ใจว่ามีการเลือกไดเรกทอรีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="51ca9-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="51ca9-133">บนเมนูด้านซ้าย ให้เลือก **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="51ca9-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="51ca9-134">ภายใต้ **จัดการ** เลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="51ca9-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="51ca9-135">รหัสผู้เช่า Azure AD ของคุณปรากฏภายใต้ **รหัสไดเรกทอรี**</span><span class="sxs-lookup"><span data-stu-id="51ca9-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="51ca9-136">ค้นหารหัสผู้เช่า Azure AD ของคุณโดยการใช้ข้อมูลเมตา OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="51ca9-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="51ca9-137">สร้าง URL ของ OpenID โดยการแทนที่ **\{YOUR\_DOMAIN\}** ด้วยโดเมนของคุณ เช่น `microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="51ca9-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="51ca9-138">ตัวอย่างเช่น `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` จะกลายเป็น `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`</span><span class="sxs-lookup"><span data-stu-id="51ca9-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="51ca9-139">ไปที่ URL ของ OpenID ที่มีโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="51ca9-140">คุณสามารถค้นหารหัสผู้เช่า Azure AD ของคุณได้ในค่าคุณสมบัติหลายค่า</span><span class="sxs-lookup"><span data-stu-id="51ca9-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="51ca9-141">ค้นหา **authorization\_endpoint** และแยก GUID ที่ปรากฏทันทีหลังจาก `login.microsoftonline.com/`</span><span class="sxs-lookup"><span data-stu-id="51ca9-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="51ca9-142">ค้นหารหัสกลุ่มรักษาความปลอดภัย Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="51ca9-143">รหัสของกลุ่มความปลอดภัย Azure AD ของคุณคือ GUID ซึ่งคล้ายกับตัวอย่างนี้: **436ea7f5-ee6c-40c1-9f08-825c5811066a**</span><span class="sxs-lookup"><span data-stu-id="51ca9-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="51ca9-144">กระบวนงานนี้สันนิษฐานว่าคุณเป็นสมาชิกของกลุ่มที่คุณกำลังพยายามค้นหารหัสให้</span><span class="sxs-lookup"><span data-stu-id="51ca9-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="51ca9-145">เปิด [ตัวสำรวจกราฟ](https://developer.microsoft.com/graph/graph-explorer#)</span><span class="sxs-lookup"><span data-stu-id="51ca9-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="51ca9-146">เลือก **ลงชื่อเข้าใช้ด้วย Microsoft** และลงชื่อเข้าใช้โดยใช้ข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="51ca9-147">ที่ด้านซ้าย ให้เลือก**แสดงตัวอย่างเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="51ca9-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="51ca9-148">ในบานหน้าต่างด้านขวา เปิดใช้งาน **กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="51ca9-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="51ca9-149">ปิดบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="51ca9-149">Close the right pane.</span></span>
1. <span data-ttu-id="51ca9-150">เลือก **ทุกกลุ่มที่ฉันเป็นสมาชิกอยู่**</span><span class="sxs-lookup"><span data-stu-id="51ca9-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="51ca9-151">ในฟิลด์ **การแสดงตัวอย่างการตอบ** ให้ค้นหากลุ่มของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="51ca9-152">รหัสกลุ่มความปลอดภัยจะปรากฏภายใต้คุณสมบัติ **รหัส**</span><span class="sxs-lookup"><span data-stu-id="51ca9-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="51ca9-153">เตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="51ca9-154">กระบวนงานเหล่านี้จะอธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="51ca9-155">หลังจากที่คุณดำเนินการเสร็จสมบูรณ์แล้ว สภาพแวดล้อมของการแสดงตัวอย่างของ Commerce จะพร้อมสำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="51ca9-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="51ca9-156">กิจกรรมทั้งหมดที่อธิบายไว้ที่นี่จะเกิดขึ้นในพอร์ทัล LCS</span><span class="sxs-lookup"><span data-stu-id="51ca9-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51ca9-157">การเข้าถึงการแสดงตัวอย่างจะเชื่อมโยงกับบัญชี LCS และองค์กรที่คุณระบุไว้ในแอพลิเคชันการแสดงตัวอย่างของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="51ca9-158">คุณต้องใช้บัญชีเดียวกันเพื่อเตรียมใช้งานสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="51ca9-159">ถ้าคุณต้องใช้บัญชี LCS หรือผู้เช่าที่แตกต่างกันสำหรับสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce คุณต้องให้รายละเอียดเหล่านั้นไปยัง Microsoft</span><span class="sxs-lookup"><span data-stu-id="51ca9-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="51ca9-160">สำหรับข้อมูลผู้ติดต่อ โปรดดูส่วน [การสนับสนุนสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](#commerce-preview-environment-support) ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="51ca9-161">ให้สิทธิการเข้าถึงแอปพลิเคชันอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="51ca9-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51ca9-162">บุคคลที่ลงชื่อเข้าใช้ต้องเป็นผู้ดูแลระบบผู้เช่า Azure AD ที่มีรหัสผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="51ca9-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="51ca9-163">หากขั้นตอนนี้ไม่เสร็จสมบูรณ์ ขั้นตอนการเตรียมใช้งานที่เหลือจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="51ca9-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="51ca9-164">ในการอนุมัติให้แอพลิเคชันอีคอมเมิร์ซเข้าถึงการสมัครใช้งาน Azure ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-165">ประกอบ URL ในรูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="51ca9-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="51ca9-166">คัดลอกและวาง URL ลงในเบราว์เซอร์หรือตัวแก้ไขข้อความของคุณ และแทนที่ **\{AAD\_TENANT\_ID\}** ด้วยรหัสผู้เช่า Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="51ca9-167">จากนั้น เปิด URL</span><span class="sxs-lookup"><span data-stu-id="51ca9-167">Then open the URL.</span></span>
1. <span data-ttu-id="51ca9-168">ในกล่องโต้ตอบการลงชื่อเข้าใช้ Azure AD ให้ลงชื่อเข้าใช้ และยืนยันว่าคุณต้องการให้สิทธิ์การเข้าถึง **Dynamics 365 Commerce (การแสดงตัวอย่าง)** ไปยังการสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="51ca9-169">คุณจะถูกส่งไปยังหน้าที่บ่งชี้ว่าการดำเนินงานนี้ประสบความสำเร็จหรือไม่</span><span class="sxs-lookup"><span data-stu-id="51ca9-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="51ca9-170">ยืนยันว่าคุณลักษณะการแสดงตัวอย่างพร้อมใช้งานและถูกเปิดใช้งานใน LCS</span><span class="sxs-lookup"><span data-stu-id="51ca9-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="51ca9-171">เพื่อยืนยันว่าคุณลักษณะการแสดงตัวอย่างพร้อมใช้งานและถูกเปิดใช้งานใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-172">ลงชื่อเข้าใช้ [พอร์ทัล LCS](https://lcs.dynamics.com) โดยใช้บัญชี LCS เดียวกันกับที่คุณใช้ในการร้องขอการเข้าถึงไปยังการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="51ca9-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="51ca9-173">ในโฮมเพจของ LCS ให้เลื่อนไปทางขวาสุด และเลือกไทล์ **การจัดการคุณลักษณะการแสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="51ca9-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![ดูตัวอย่างไทล์การจัดการ](./media/preview1.png)

1. <span data-ttu-id="51ca9-175">เลื่อนลงไปที่ **คุณลักษณะการแสดงตัวอย่างส่วนตัว** และยืนยันว่าคุณลักษณะต่อไปนี้พร้อมใช้งานและถูกเปิดใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="51ca9-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="51ca9-176">การประเมินอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="51ca9-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="51ca9-177">สภาพแวดล้อมของโปรแกรมตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-177">Commerce Preview Program Environments</span></span>

    ![คุณลักษณะแสดงตัวอย่างแบบส่วนตัว](./media/preview2.png)

1. <span data-ttu-id="51ca9-179">ถ้าคุณลักษณะเหล่านั้นไม่ปรากฏในรายการ โปรดติดต่อ Microsoft และระบุที่อยู่อีเมลที่ทำงานของคุณ บัญชี LCS และรายละเอียดผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="51ca9-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="51ca9-180">สำหรับข้อมูลผู้ติดต่อ โปรดดูส่วน [การสนับสนุนสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](#commerce-preview-environment-support)</span><span class="sxs-lookup"><span data-stu-id="51ca9-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="51ca9-181">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="51ca9-181">Create a new project</span></span>

<span data-ttu-id="51ca9-182">เมื่อต้องการสร้างโครงการใหม่ใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-183">บนโฮมเพจ LCS ให้เลือกเครื่องหมายบวก (**+**) เพื่อสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="51ca9-184">ในบานหน้าต่างด้านขวา ให้ทำตามหนึ่งในขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="51ca9-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="51ca9-185">ถ้าคุณเป็นคู่ค้า ให้เลือก **โยกย้าย สร้างวิธีแก้ไข และเรียนรู้**</span><span class="sxs-lookup"><span data-stu-id="51ca9-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="51ca9-186">ถ้าคุณเป็นลูกค้า ให้เลือก **การเปิดจำหน่ายล่วงหน้าสำหรับผู้ที่มีแนวโน้มจะเป็นลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="51ca9-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="51ca9-187">ป้อนชื่อ คำอธิบาย และอุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="51ca9-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="51ca9-188">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้เลือก **Dynamics 365 Retail**</span><span class="sxs-lookup"><span data-stu-id="51ca9-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="51ca9-189">ในฟิลด์ **รุ่นผลิตภัณฑ์** ให้เลือก **Dynamics 365 Retail**</span><span class="sxs-lookup"><span data-stu-id="51ca9-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="51ca9-190">ในฟิลด์ **วิธีการ** ให้เลือก **วิธีการใช้งานการขายปลีกของ Dynamics**</span><span class="sxs-lookup"><span data-stu-id="51ca9-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="51ca9-191">ไม่จำเป็นต้องระบุ: คุณสามารถนำเข้าบทบาทและผู้ใช้จากโครงการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="51ca9-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="51ca9-192">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="51ca9-192">Select **Create**.</span></span> <span data-ttu-id="51ca9-193">มุมมองโครงการจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="51ca9-194">เพิ่มตัวเชื่อมต่อ Azure</span><span class="sxs-lookup"><span data-stu-id="51ca9-194">Add the Azure Connector</span></span>

<span data-ttu-id="51ca9-195">ในการเพิ่มตัวเชื่อมต่อ Azure ไปยังโครงการ LCS ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-196">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="51ca9-197">หากคุณเป็นคู่ค้า ให้เลือกไทล์ **การตั้งค่าโครงการ** ที่ด้านขวาสุด</span><span class="sxs-lookup"><span data-stu-id="51ca9-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="51ca9-198">ถ้าคุณเป็นลูกค้า ให้เลือก **การตั้งค่าโครงการ** บนเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="51ca9-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="51ca9-199">เลือก **ตัวเชื่อมต่อ Azure**</span><span class="sxs-lookup"><span data-stu-id="51ca9-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="51ca9-200">เลือก **เพิ่ม** เพื่อเพิ่มตัวเชื่อมต่อ Azure</span><span class="sxs-lookup"><span data-stu-id="51ca9-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="51ca9-201">ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="51ca9-201">Enter a name.</span></span>
1. <span data-ttu-id="51ca9-202">ป้อนรหัสการสมัครใช้งาน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="51ca9-203">เปิดใช้งานตัวเลือก **ตั้งค่าคอนฟิกเพื่อใช้ Azure Resource Manager (ARM)**</span><span class="sxs-lookup"><span data-stu-id="51ca9-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="51ca9-204">ตรวจสอบว่าค่า **โดเมน (หรือรหัส) ผู้เช่า AAD ในการสมัครใช้งาน Azure AAD** ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="51ca9-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="51ca9-205">โปรดปรึกษาผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="51ca9-206">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="51ca9-206">Select **Next**.</span></span>
1. <span data-ttu-id="51ca9-207">ทำตามคำแนะนำบนหน้าเพื่อให้สิทธิ์การเข้าถึงแอพลิเคชันที่จำเป็นแก่การสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="51ca9-208">โปรดปรึกษาผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="51ca9-209">ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="51ca9-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="51ca9-210">ตรวจสอบให้แน่ใจว่าได้เลือกไดเรกทอรีที่ถูกต้อง และจากนั้น บนเมนูทางซ้ายให้เลือก **การสมัครใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="51ca9-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="51ca9-211">ค้นหาการสมัครเข้าใช้งานที่ถูกต้องในรายการ แล้วเลือกรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="51ca9-212">ใช้ฟังก์ชันการค้นหาตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="51ca9-213">บนเมนู เลือก **การควบคุมการเข้าถึง (IAM)**</span><span class="sxs-lookup"><span data-stu-id="51ca9-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="51ca9-214">ทางด้านขวา ภายใต้ **เพิ่มการกำหนดบทบาท** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="51ca9-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="51ca9-215">บานหน้าต่าง **เพิ่มการกำหนดบทบาท** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="51ca9-216">ในฟิลด์ **บทบาท** ให้เลือก **ผู้สนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="51ca9-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="51ca9-217">ในฟิลด์ **กำหนดการเข้าถึงไปยัง** ให้ละทิ้งค่าเริ่มต้น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**</span><span class="sxs-lookup"><span data-stu-id="51ca9-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="51ca9-218">ภายใต้ **เลือก** ให้ป้อน **b96b7e94-b82e-4e71-99a0-cf7fb188acea**</span><span class="sxs-lookup"><span data-stu-id="51ca9-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="51ca9-219">เลือก **Dynamics Deployment Services \[wsfed-enabled\]** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="51ca9-220">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="51ca9-220">Select **Save**.</span></span>

1. <span data-ttu-id="51ca9-221">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="51ca9-221">Select **Next**.</span></span>
1. <span data-ttu-id="51ca9-222">ทำตามคำแนะนำบนหน้าเพื่อให้สิทธิ์การเข้าถึงแอพลิเคชันที่จำเป็นแก่การสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="51ca9-223">โปรดปรึกษาผู้ดูแลระบบการสมัครใช้งาน Azure ของคุณตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="51ca9-224">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="51ca9-224">Select **Next**.</span></span>
1. <span data-ttu-id="51ca9-225">ในฟิลด์ **ภูมิภาคของ Azure** เลือก **สหรัฐอเมริกาตะวันออก** **สหรัฐอเมริกาตะวันออก 2** **สหรัฐอเมริกาตะวันตก** หรือ **สหรัฐอเมริกาตะวันตก 2**</span><span class="sxs-lookup"><span data-stu-id="51ca9-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="51ca9-226">เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="51ca9-226">Select **Connect**.</span></span> <span data-ttu-id="51ca9-227">ตัวเชื่อมต่อ Azure ของคุณน่าจะปรากฏขึ้นในรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="51ca9-228">นำเข้าส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="51ca9-229">ถ้าต้องการนำเข้าส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce ลงในโครงการของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-230">เปิดโฮมเพจสำหรับโครงการของคุณโดยการเลือกชื่อโครงการที่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="51ca9-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="51ca9-231">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="51ca9-232">หากคุณเป็นคู่ค้า ให้เลือกไทล์ **ไลบรารีแอสเซท** ที่ด้านขวาสุด</span><span class="sxs-lookup"><span data-stu-id="51ca9-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="51ca9-233">ถ้าคุณเป็นลูกค้า ให้เลือก **ไลบรารีแอสเซท** บนเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="51ca9-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="51ca9-234">ในรายการทางด้านซ้าย เลือก **แพคเกจที่สามารถปรับใช้ได้ของซอฟต์แวร์**</span><span class="sxs-lookup"><span data-stu-id="51ca9-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="51ca9-235">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="51ca9-235">Select **Import**.</span></span>
1. <span data-ttu-id="51ca9-236">ภายใต้ **ไลบรารีแอสเซทที่ใช้ร่วมกัน** เลือก **ส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce** ในรายการของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="51ca9-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="51ca9-237">เลือก **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="51ca9-237">Select **Pick**.</span></span> <span data-ttu-id="51ca9-238">คุณถูกส่งกลับไปยังไลบรารีแอสเซท และคุณควรเห็นส่วนขยายในรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="51ca9-239">ภาพประกอบต่อไปนี้แสดงการดำเนินการที่ต้องดำเนินการบนหน้า **ไลบรารีแอสเซท** ของ LCS</span><span class="sxs-lookup"><span data-stu-id="51ca9-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![การนำเข้าส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="51ca9-241">ปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="51ca9-241">Deploy the environment</span></span>

<span data-ttu-id="51ca9-242">เพื่อปรับใช้สภาพแวดล้อม ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="51ca9-243">คุณอาจไม่จำเป็นต้องทำตามขั้นตอนที่ 6 7 และ/หรือ 8 ให้เสร็จสมบูรณ์ เนื่องจากเพจที่มีตัวเลือกเดียวจะถูกข้ามไป</span><span class="sxs-lookup"><span data-stu-id="51ca9-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="51ca9-244">เมื่อคุณอยู่ในมุมมอง **พารามิเตอร์สภาพแวดล้อม** ให้ยืนยันว่าข้อความ **Dynamics 365 Commerce (การแสดงตัวอย่าง) - สาธิต (10.0.6 ที่มีการอัพเดตแพลตฟอร์ม 30)** จะปรากฏขึ้นเหนือฟิลด์ **ชื่อสภาพแวดล้อม** โดยตรง</span><span class="sxs-lookup"><span data-stu-id="51ca9-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="51ca9-245">ดูภาพประกอบที่ปรากฏหลังจากขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="51ca9-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="51ca9-246">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="51ca9-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="51ca9-247">เลือก **เพิ่ม** เพื่อเพิ่มสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="51ca9-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="51ca9-248">ในฟิลด์ **รุ่นแอพลิเคชัน** ให้เลือก **10.0.6**</span><span class="sxs-lookup"><span data-stu-id="51ca9-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="51ca9-249">ในฟิลด์ **รุ่นแพลตฟอร์ม** ให้เลือก **การอัพเดตแพลตฟอร์ม 30**</span><span class="sxs-lookup"><span data-stu-id="51ca9-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![การเลือกรุ่นของแอพลิเคชันและแพลตฟอร์ม](./media/project1.png)

1. <span data-ttu-id="51ca9-251">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="51ca9-251">Select **Next**.</span></span>
1. <span data-ttu-id="51ca9-252">เลือก **สาธิต** เป็นโทโพโลยีสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="51ca9-252">Select **Demo** as the environment topology.</span></span>

    ![การเลือกโทโพโลยีสภาพแวดล้อม 1](./media/project2.png)

1. <span data-ttu-id="51ca9-254">เลือก **Dynamics 365 Commerce (การแสดงตัวอย่าง) - สาธิต** เป็นโทโพโลยีสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="51ca9-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="51ca9-255">ถ้าคุณได้ตั้งค่าคอนฟิกตัวเชื่อมต่อ Azure แบบเดี่ยวก่อนหน้านี้แล้ว จะมีการใช้สำหรับสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="51ca9-256">ถ้าคุณตั้งค่าคอนฟิกตัวเชื่อมต่อ Azure ที่หลากหลาย คุณสามารถเลือกตัวเชื่อมต่อที่จะใช้: **สหรัฐอเมริกาตะวันออก** **สหรัฐอเมริกาตะวันออก 2** **สหรัฐอเมริกาตะวันตก 2** หรือ **สหรัฐอเมริกาตะวันตก 2**</span><span class="sxs-lookup"><span data-stu-id="51ca9-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="51ca9-257">สำหรับประสิทธิภาพการทำงานแบบครอบคลุมที่ดีที่สุด เราขอแนะนำให้คุณเลือก **สหรัฐอเมริกาตะวันตก 2**)</span><span class="sxs-lookup"><span data-stu-id="51ca9-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![การเลือกโทโพโลยีสภาพแวดล้อม 2](./media/project3.png)

1. <span data-ttu-id="51ca9-259">บนเพจ **ปรับใช้สภาพแวดล้อม** ให้ป้อนชื่อสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="51ca9-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="51ca9-260">ปล่อยการตั้งค่าขั้นสูงไว้ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="51ca9-260">Leave the advanced settings as they are.</span></span>

    ![ปรับใช้เพจสภาพแวดล้อม](./media/project4.png)

1. <span data-ttu-id="51ca9-262">ปรับขนาด VM ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-262">Adjust the VM size as required.</span></span> <span data-ttu-id="51ca9-263">(เราขอแนะนำหน่วยการเก็บสต็อกสินค้า VM \[SKU\] **D13 v2**)</span><span class="sxs-lookup"><span data-stu-id="51ca9-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="51ca9-264">ตรวจสอบเงื่อนไขการกำหนดราคาและการให้สิทธิ์การใช้งาน และจากนั้น เลือกกล่องกาเครื่องหมายเพื่อบ่งชี้ว่าคุณเห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="51ca9-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="51ca9-265">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="51ca9-265">Select **Next**.</span></span>
1. <span data-ttu-id="51ca9-266">บนหน้ายืนยันการปรับใช้ ตรวจสอบว่ารายละเอียดทั้งหลายถูกต้อง และจากนั้น เลือก **ปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="51ca9-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="51ca9-267">คุณจะกลับไปยังมุมมอง **สภาพแวดล้อมที่ใช้ Cloud** และสภาพแวดล้อมของคุณควรจะปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="51ca9-268">สภาพแวดล้อมที่ร้องขอของคุณจะปรากฎเป็นอยู่ในคิว และจากนั้นจะเปลี่ยนเป็นกำลังปรับใช้</span><span class="sxs-lookup"><span data-stu-id="51ca9-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="51ca9-269">เวิร์กโฟลว์สภาพแวดล้อมจะใช้เวลาสักครู่เพื่อให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="51ca9-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="51ca9-270">ดังนั้น โปรดกลับมาตรวจสอบหลังจากประมาณหกถึงเก้าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="51ca9-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="51ca9-271">ก่อนที่คุณจะดำเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าสถานะของสภาพแวดล้อมของคุณคือ **ปรับใช้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="51ca9-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="51ca9-272">ตั้งค่าเพื่อเริ่มใช้งาน RCSU</span><span class="sxs-lookup"><span data-stu-id="51ca9-272">Initialize RCSU</span></span>

<span data-ttu-id="51ca9-273">เมื่อต้องการเริ่มต้น RCSU ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-274">ในมุมมอง **สภาพแวดล้อมที่ใช้ Cloud** ให้เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="51ca9-275">ในมุมมองสภาพแวดล้อมทางด้านขวา เลือก **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="51ca9-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="51ca9-276">มุมมองรายละเอียดของสภาพแวดล้อมจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-276">The environment details view appears.</span></span>
1. <span data-ttu-id="51ca9-277">ภายใต้ **คุณลักษณะของสภาพแวดล้อม** ให้เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="51ca9-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="51ca9-278">บนแท็บ **Retail** ให้เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="51ca9-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="51ca9-279">มุมมองพารามิเตอร์สำหรับการเริ่มต้นใช้งาน RCSU จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="51ca9-280">ในฟิลด์ **ภูมิภาค** เลือก **สหรัฐอเมริกาตะวันออก** **สหรัฐอเมริกาตะวันออก 2** **สหรัฐอเมริกาตะวันตก** หรือ **สหรัฐอเมริกาตะวันตก 2**</span><span class="sxs-lookup"><span data-stu-id="51ca9-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="51ca9-281">ในฟิลด์ **รุ่น** ให้เลือก **ระบุรุ่น** ในรายการ และจากนั้น ระบุ **9.16.19262.5** ในฟิลด์ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="51ca9-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="51ca9-282">ตรวจสอบให้แน่ใจว่าได้ระบุรุ่นที่แน่นอนซึ่งถูกระบุไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="51ca9-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="51ca9-283">มิฉะนั้น คุณจะต้องปรับปรุง RCSU เป็นรุ่นที่ถูกต้องในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="51ca9-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="51ca9-284">เปิดใช้งานตัวเลือก **ใช้ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="51ca9-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="51ca9-285">ในรายการส่วนขยาย ให้เลือก **ส่วนขยายพื้นฐานของการสาธิตตัวอย่างของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="51ca9-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="51ca9-286">เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="51ca9-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="51ca9-287">บนหน้ายืนยันการปรับใช้ ตรวจสอบว่ารายละเอียดทั้งหลายถูกต้อง และจากนั้น เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="51ca9-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="51ca9-288">คุณจะถูกส่งกลับไปยังมุมมอง **การจัดการการขายปลีก** ที่ซึ่งมีการเลือกแท็บ **Retail**</span><span class="sxs-lookup"><span data-stu-id="51ca9-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="51ca9-289">RCSU ของคุณได้รับการจัดคิวสำหรับการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51ca9-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="51ca9-290">ก่อนที่คุณจะดำเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าสถานะของ RCSU ของคุณคือ **สำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="51ca9-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="51ca9-291">การเริ่มต้นใช้งานจะใช้เวลาประมาณสองถึงห้าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="51ca9-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="51ca9-292">ตั้งค่าเพื่อเริ่มต้นใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="51ca9-292">Initialize e-Commerce</span></span>

<span data-ttu-id="51ca9-293">เมื่อต้องการเริ่มต้นอีคอมเมิร์ซ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="51ca9-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51ca9-294">บนแท็บ **อีคอมเมิร์ซ (การแสดงตัวอย่าง)** ให้ตรวจสอบความยินยอมในการแสดงตัวอย่าง และจากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="51ca9-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="51ca9-295">ในฟิลด์ **ชื่อผู้เช่าอีคอมเมิร์ซ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="51ca9-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="51ca9-296">อย่างไรก็ตาม โปรดทราบว่าชื่อนี้จะปรากฏในบาง URL ที่ชี้ไปยังอินสแตนซ์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="51ca9-297">ในฟิลด์ **ชื่อ Retail Cloud Scale Unit** เลือก RCSU ของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="51ca9-298">(รายการควรมีเพียงตัวเลือกเดียว)</span><span class="sxs-lookup"><span data-stu-id="51ca9-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="51ca9-299">ฟิลด์ **ภูมิศาสตร์ของอีคอมเมิร์ซ** ถูกตั้งค่าโดยอัตโนมัติ และไม่สามารถเปลี่ยนค่าได้</span><span class="sxs-lookup"><span data-stu-id="51ca9-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="51ca9-300">เลือก **ถัดไป** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="51ca9-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="51ca9-301">ในฟิลด์ **ชื่อโฮสต์ที่ได้รับการสนับสนุน** ให้ป้อนโดเมนที่ถูกต้องใดๆ เช่น `www.fabrikam.com`</span><span class="sxs-lookup"><span data-stu-id="51ca9-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="51ca9-302">ในฟิลด์ **กลุ่มความปลอดภัย AAD สำหรับผู้ดูแลระบบ** ให้ป้อนอักษรสองสามตัวแรกของชื่อของกลุ่มความปลอดภัยที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="51ca9-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="51ca9-303">เลือกไอคอนคลาสการขยายเพื่อแสดงผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="51ca9-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="51ca9-304">เลือกกลุ่มความปลอดภัยจากรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="51ca9-305">ในฟิลด์ **กลุ่มความปลอดภัย AAD สำหรับการให้คะแนนและตรวจสอบผู้ตรวจสอบ** ให้ป้อนอักษรสองสามตัวแรกของชื่อของกลุ่มความปลอดภัยที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="51ca9-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="51ca9-306">เลือกไอคอนคลาสการขยายเพื่อแสดงผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="51ca9-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="51ca9-307">เลือกกลุ่มความปลอดภัยจากรายการ</span><span class="sxs-lookup"><span data-stu-id="51ca9-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="51ca9-308">ปล่อยให้ตัวเลือก **เปิดใช้งานบริการการให้คะแนนและบทวิจารณ์** เปิด</span><span class="sxs-lookup"><span data-stu-id="51ca9-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="51ca9-309">ถ้าคุณได้ดำเนินการขั้นตอนความยินยอมของ Microsoft Azure Active Directory (Azure AD) เสร็จสิ้น ตามที่อธิบายไว้ในส่วน "ให้สิทธิ์การเข้าถึงไปยังแอพลิเคชันอีคอมเมิร์ซ" ให้เลือกกล่องกาเครื่องหมายเพื่อยืนยันความยินยอมของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="51ca9-310">หากคุณยังไม่ได้ทำขั้นตอนนี้ให้เสร็จสมบูรณ์ คุณจำเป็นต้องดำเนินการดังกล่าวก่อนที่จะดำเนินการกับการเริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="51ca9-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="51ca9-311">เลือกการเชื่อมโยงภายในข้อความที่อยู่ถัดจากกล่องกาเครื่องหมาย เพื่อเปิดกล่องโต้ตอบความยินยอมและทำขั้นตอนให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="51ca9-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="51ca9-312">เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="51ca9-312">Select **Initialize**.</span></span> <span data-ttu-id="51ca9-313">คุณจะถูกส่งกลับไปยังมุมมอง **การจัดการการขายปลีก** ที่ซึ่งมีการเลือกแท็บ **อีคอมเมิร์ซ (การแสดงตัวอย่าง)**</span><span class="sxs-lookup"><span data-stu-id="51ca9-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="51ca9-314">การเริ่มใช้งานอีคอมเมิร์ซได้เริ่มต้นขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="51ca9-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="51ca9-315">ก่อนที่คุณจะดำเนินการต่อไป ให้รอจนกว่าสถานะของการเริ่มต้นใช้งานอีคอมเมิร์ซจะเป็น **การเริ่มต้นใช้งานสำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="51ca9-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="51ca9-316">ภายใต้ **ลิงค์** ที่ด้านล่างขวา ให้จดบันทึก URL สำหรับลิงค์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="51ca9-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="51ca9-317">**ไซต์อีคอมเมิร์ซ** – การเชื่อมโยงไปยังรากของไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="51ca9-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="51ca9-318">**เครื่องมือการจัดการไซต์อีคอมเมิร์ซ** – การเชื่อมโยงไปยังเครื่องมือการจัดการไซต์</span><span class="sxs-lookup"><span data-stu-id="51ca9-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="51ca9-319">การสนับสนุนสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-319">Commerce preview environment support</span></span>

<span data-ttu-id="51ca9-320">ถ้าคุณประสบปัญหาขณะที่คุณกำลังดำเนินการขั้นตอนการจัดเตรียมให้เสร็จสมบูรณ์ โปรดเยี่ยมชม [กลุ่ม Microsoft Dynamics 365 Commerce Preview Yammer](https://aka.ms/Dynamics365CommercePreviewYammer) สำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="51ca9-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="51ca9-321">ถ้าคุณพบปัญหาเมื่อคุณพยายามเข้าถึงกลุ่ม Yammer คุณสามารถติดต่อ Microsoft ทางอีเมลได้ที่ <Dynamics365Commerce@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="51ca9-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="51ca9-322">ที่อยู่อีเมลนี้ไม่ได้ตรวจสอบอย่างแข็งขัน.</span><span class="sxs-lookup"><span data-stu-id="51ca9-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="51ca9-323">ดังนั้นคาดว่าจะมีการหน่วงเวลาในการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="51ca9-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51ca9-324">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="51ca9-324">Next steps</span></span>

<span data-ttu-id="51ca9-325">เพื่อดำเนินการกระบวนการในการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce ของคุณต่อ ให้ดูที่ [ตั้งค่าคอนฟิกสภาพแวดล้อมของการแสดงตัวอย่างของ Commerce](cpe-post-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="51ca9-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51ca9-326">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="51ca9-326">Additional resources</span></span>

[<span data-ttu-id="51ca9-327">ภาพรวมของสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="51ca9-328">กำหนดค่าสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="51ca9-329">กำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="51ca9-330">FAQ เกี่ยวกับสภาพแวดล้อมการแสดงตัวอย่างของ Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="51ca9-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="51ca9-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="51ca9-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="51ca9-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="51ca9-333">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="51ca9-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="51ca9-334">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="51ca9-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="51ca9-335">แหล่งข้อมูลความช่วยเหลือสำหรับ Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="51ca9-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
