---
title: ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างหน้าแบบกำหนดเองใน Microsoft Dynamics 365 Commerce ที่จัดการการลงชื่อเข้าใช้สำหรับผู้ใช้ของ Azure Active Directory (Azure AD) ที่เป็นผู้เช่าธุรกิจ-ลูกค้า (B2C)
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0b54bf6234dcb87c84b21259c30ca5c321869adf
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817317"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="7f01f-103">ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7f01f-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7f01f-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างหน้าแบบกำหนดเองใน Microsoft Dynamics 365 Commerce ที่จัดการการลงชื่อเข้าใช้สำหรับผู้ใช้ของ Azure Active Directory (Azure AD) ที่เป็นผู้เช่าธุรกิจ-ลูกค้า (B2C)</span><span class="sxs-lookup"><span data-stu-id="7f01f-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="7f01f-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="7f01f-105">Overview</span></span>

<span data-ttu-id="7f01f-106">เมื่อต้องการใช้หน้าแบบกำหนดเองที่มีการสร้างใน Dynamics 365 Commerce เพื่อจัดการขั้นตอนการลงชื่อเข้า คุณต้องตั้งค่านโยบาย Azure AD ที่จะถูกอ้างอิงในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="7f01f-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="7f01f-107">คุณสามารถตั้งค่าคอนฟิก "ลงทะเบียนและลงชื่อเข้าใช้" "แก้ไขโพรไฟล์" และ "รีเซ็ตรหัสผ่าน" นโยบาย B2C Azure AD โดยใช้แอพลิเคชัน B2C Azure AD</span><span class="sxs-lookup"><span data-stu-id="7f01f-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="7f01f-108">ชื่อผู้เช่าและนโยบาย B2C Azure AD สามารถอ้างอิงในระหว่างกระบวนการเตรียมใช้งานที่ทำไว้สำหรับสภาพแวดล้อม Commerce โดยใช้วงจรชีวิต Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="7f01f-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="7f01f-109">หน้า Commerce ที่กำหนดเองสามารถสร้างได้โดยใช้การลงชื่อเข้าใช้ ลงทะเบียน การแก้ไขโพรไฟล์บัญชี หรือโมดูลการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="7f01f-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="7f01f-110">Url ของหน้าซึ่งเผยแพร่สำหรับหน้าแบบกำหนดเองเหล่านี้ควรจะถูกอ้างอิงในการตั้งค่าคอนฟิกนโยบาย B2C Azure AD ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="7f01f-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="7f01f-111">ตั้งค่านโยบาย B2C</span><span class="sxs-lookup"><span data-stu-id="7f01f-111">Set up B2C policies</span></span>

<span data-ttu-id="7f01f-112">หลังจากที่คุณตั้งค่าผู้เช่า B2C Azure AD ของคุณ และเชื่อมโยงกับสภาพแวดล้อม Commerce ให้ไปที่หน้า **Azure AD B2C** ในพอร์ทัล Azure จากนั้นบนเมนูภายใต้ **นโยบาย** ให้เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)**</span><span class="sxs-lookup"><span data-stu-id="7f01f-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![คำสั่งขั้นตอนของผู้ใช้ (นโยบาย) บนเมนู](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="7f01f-114">ขณะนี้คุณสามารถตั้งค่าคอนฟิก "ลงทะเบียนและลงชื่อเข้าใช้" "แก้ไขโพรไฟล์" และ "รีเซ็ตรหัสผ่าน" ผู้ใช้ในขั้นตอนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="7f01f-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="7f01f-115">ตั้งค่าคอนฟิกนโยบาย "การลงทะเบียนและลงชื่อเข้าใช้"</span><span class="sxs-lookup"><span data-stu-id="7f01f-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="7f01f-116">เมื่อต้องการตั้งค่าคอนฟิกนโยบาย "การลงชื่อเข้าใช้และลงทะเบียน" ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-117">เลือก **ขั้นตอนของผู้ใช้ใหม่** จากนั้นบนแท็บ **ที่แนะนำ** เลือกนโยบาย **การลงทะเบียนและลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="7f01f-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="7f01f-118">ป้อนชื่อสำหรับนโยบาย (ตัวอย่างเช่น **B2C\_1\_SignInSignUp**)</span><span class="sxs-lookup"><span data-stu-id="7f01f-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="7f01f-119">ในส่วน **ตัวให้บริการข้อมูลเฉพาะตัว** เลือกผู้ให้บริการข้อมูลเฉพาะตัวที่จะใช้สำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="7f01f-120">อย่างน้อยที่สุด ต้องมีการเลือก **ลงทะเบียนอีเมล**</span><span class="sxs-lookup"><span data-stu-id="7f01f-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="7f01f-121">ในคอลัมน์ **รวบรวมแอททริบิวต์** เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** และ **นามสกุล**</span><span class="sxs-lookup"><span data-stu-id="7f01f-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="7f01f-122">ในคอลัมน์ **การอ้างสิทธิ์การส่งคืนสินค้า** ให้เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** **ตัวให้บริการข้อมูลเฉพาะตัว** **นามสกุล** และ **รหัสออบเจ็กต์ของผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="7f01f-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![แอททริบิวต์และการอ้างสิทธิ์ที่เลือก](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="7f01f-124">เลือก **ตกลง** เมื่อต้องการสร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7f01f-125">ดับเบิลคลิกที่ชื่อนโยบายใหม่ จากนั้นในบานหน้าต่างนำทางให้เลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="7f01f-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7f01f-126">ตั้งค่าตัวเลือก **เปิดใช้งานโครงร่างหน้าการบังคับใช้ JavaScript (การแสดงตัวอย่าง)** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="7f01f-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![หน้าคุณสมบัติสำหรับนโยบายใหม่](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="7f01f-128">ชื่อนโยบายจะถูกอ้างอิงทั้งหมดในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="7f01f-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="7f01f-129">(คำนำหน้า **B2C\_1\_** จะรวมอยู่ในการอ้างอิง) ไม่สามารถเปลี่ยนชื่อนโยบายหลังจากที่สร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="7f01f-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="7f01f-130">ถ้าคุณกำลังเปลี่ยนนโยบายที่มีอยู่สำหรับสภาพแวดล้อม Commerce ของคุณ คุณสามารถลบนโยบายเดิมและสร้างนโยบายใหม่ที่มีชื่อเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="7f01f-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="7f01f-131">อีกทางหนึ่งคือถ้ามีการเตรียมใช้งานสภาพแวดล้อมแล้วคุณสามารถส่งชื่อนโยบายใหม่ผ่านการร้องขอการบริการ</span><span class="sxs-lookup"><span data-stu-id="7f01f-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="7f01f-132">คุณจะกลับไปที่นโยบายนี้เพื่อดำเนินการตั้งค่าให้เสร็จสมบูรณ์หลังจากที่คุณได้สร้างหน้าแบบกำหนดเองแล้ว</span><span class="sxs-lookup"><span data-stu-id="7f01f-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7f01f-133">เมื่อต้องการทำเช่นนี้ให้ปิดนโยบายเพื่อกลับไปที่หน้า **ขั้นตอนผู้ใช้ (นโยบาย)** ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="7f01f-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="7f01f-134">ตั้งค่าคอนฟิกนโยบาย "การแก้ไขโพรไฟล์"</span><span class="sxs-lookup"><span data-stu-id="7f01f-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="7f01f-135">ในการตั้งค่าคอนฟิกนโยบาย "การแก้ไขโพรไฟล์" ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-136">เลือก **ขั้นตอนของผู้ใช้ใหม่** จากนั้นบนแท็บ **ที่แนะนำ** เลือกนโยบาย **การแก้ไขโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="7f01f-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="7f01f-137">ป้อนชื่อสำหรับนโยบาย (ตัวอย่างเช่น **B2C\_1\_EditProfile**)</span><span class="sxs-lookup"><span data-stu-id="7f01f-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="7f01f-138">ในส่วน **ตัวให้บริการข้อมูลเฉพาะตัว** เลือกผู้ให้บริการข้อมูลเฉพาะตัวที่จะใช้สำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="7f01f-139">อย่าน้อยต้องเลือก **ลงชื่อเข้าใช้บัญชีท้องถิ่น**</span><span class="sxs-lookup"><span data-stu-id="7f01f-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="7f01f-140">ในคอลัมน์ **รวบรวมแอททริบิวต์** เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** และ **นามสกุล**</span><span class="sxs-lookup"><span data-stu-id="7f01f-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="7f01f-141">ในคอลัมน์ **การอ้างสิทธิ์การส่งคืนสินค้า** ให้เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** **ตัวให้บริการข้อมูลเฉพาะตัว** **นามสกุล** และ **รหัสออบเจ็กต์ของผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="7f01f-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="7f01f-142">เลือก **ตกลง** เมื่อต้องการสร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7f01f-143">ดับเบิลคลิกที่ชื่อนโยบายใหม่ จากนั้นในบานหน้าต่างนำทางให้เลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="7f01f-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7f01f-144">ตั้งค่าตัวเลือก **เปิดใช้งานโครงร่างหน้าการบังคับใช้ JavaScript (การแสดงตัวอย่าง)** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="7f01f-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="7f01f-145">คุณจะกลับไปที่นโยบายนี้เพื่อดำเนินการตั้งค่าให้เสร็จสมบูรณ์หลังจากที่คุณได้สร้างหน้าแบบกำหนดเองแล้ว</span><span class="sxs-lookup"><span data-stu-id="7f01f-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7f01f-146">เมื่อต้องการทำเช่นนี้ให้ปิดนโยบายเพื่อกลับไปที่หน้า **ขั้นตอนผู้ใช้ (นโยบาย)** ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="7f01f-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="7f01f-147">ตั้งค่าคอนฟิกนโยบาย "รีเซ็ตรหัสผ่าน"</span><span class="sxs-lookup"><span data-stu-id="7f01f-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="7f01f-148">ในการตั้งค่าคอนฟิกนโยบาย "รีเซ็ตรหัสผ่าน" ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-149">เลือก **ขั้นตอนของผู้ใช้ใหม่** จากนั้นบนแท็บ **แสดงตัวอย่าง** เลือกนโยบาย **รีเซ็ตรหัสผ่าน v1.1**</span><span class="sxs-lookup"><span data-stu-id="7f01f-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![ตั้งค่านโยบายรหัสผ่าน v 1.1 ที่เลือกบนแท็บการแสดงตัวอย่าง](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="7f01f-151">ป้อนชื่อสำหรับนโยบาย (ตัวอย่างเช่น **B2C\_1\_ForgetPassword**)</span><span class="sxs-lookup"><span data-stu-id="7f01f-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="7f01f-152">ในส่วน **ตัวให้บริการข้อมูลเฉพาะ** เลือก **รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล**</span><span class="sxs-lookup"><span data-stu-id="7f01f-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="7f01f-153">ในคอลัมน์ **การอ้างสิทธิ์การส่งคืนสินค้า** ให้เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** **นามสกุล** และ **รหัสออบเจ็กต์ของผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="7f01f-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![การเรียกร้องที่เลือก](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="7f01f-155">เลือก **ตกลง** เมื่อต้องการสร้างนโยบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="7f01f-156">ดับเบิลคลิกที่ชื่อนโยบายใหม่ จากนั้นในบานหน้าต่างนำทางให้เลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="7f01f-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="7f01f-157">ตั้งค่าตัวเลือก **เปิดใช้งานโครงร่างหน้าการบังคับใช้ JavaScript (การแสดงตัวอย่าง)** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="7f01f-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="7f01f-158">คุณจะกลับไปที่นโยบายนี้เพื่อดำเนินการตั้งค่าให้เสร็จสมบูรณ์หลังจากที่คุณได้สร้างหน้าแบบกำหนดเองแล้ว</span><span class="sxs-lookup"><span data-stu-id="7f01f-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="7f01f-159">เมื่อต้องการทำเช่นนี้ให้ปิดนโยบายเพื่อกลับไปที่หน้า **ขั้นตอนผู้ใช้ (นโยบาย)** ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="7f01f-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="7f01f-160">สร้างหน้าแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7f01f-160">Build the custom pages</span></span>

<span data-ttu-id="7f01f-161">เมื่อต้องการสร้างหน้าแบบกำหนดเองเพื่อจัดการการลงชื่อเข้าใช้ของผู้ใช้ให้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-162">ในสภาพแวดล้อมการสร้างเครื่องมือ ให้ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f01f-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="7f01f-163">สร้างห้าเท็มเพลตและห้าหน้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f01f-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="7f01f-164">เท็มเพลต **ลงชื่อเข้าใช้** และหน้าที่ใช้โมดูลลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="7f01f-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="7f01f-165">เท็มเพลต **ลงทะเบียน** และหน้าที่ใช้โมดูลลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="7f01f-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="7f01f-166">เท็มเพลต **รีเซ็ตรหัสผ่าน** และหน้าที่ใช้โมดูลการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="7f01f-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="7f01f-167">เท็มเพลต **การตรวจสอบความถูกต้องของการรีเซ็ตรหัสผ่าน** และหน้าที่ใช้โมดูลการตรวจสอบความถูกต้องของการรีเซ็ตรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="7f01f-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="7f01f-168">เท็มเพลต **การแก้ไขโพรไฟล์** และหน้าที่ใช้ในโมดูลการแก้ไขโพรไฟล์บัญชี</span><span class="sxs-lookup"><span data-stu-id="7f01f-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="7f01f-169">เมื่อคุณสร้างหน้า ให้ปฏิบัติตามคำแนะนำต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="7f01f-170">สำหรับแต่ละหน้าหรือโมดูล ให้ใช้โครงร่างและลักษณะที่ตรงกับความต้องการของธุรกิจของคุณมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="7f01f-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="7f01f-171">เผยแพร่หน้าและ Url ทั้งหมดที่ต้องใช้ในการตั้งค่า B2C Azure AD</span><span class="sxs-lookup"><span data-stu-id="7f01f-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="7f01f-172">หลังจากเผยแพร่หน้าและ Url แล้วให้รวบรวม Url ที่ต้องใช้สำหรับการตั้งค่าคอนฟิกนโยบาย B2C Azure AD</span><span class="sxs-lookup"><span data-stu-id="7f01f-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="7f01f-173">A **?preloadscripts=true** คำต่อท้ายจะถูกเพิ่มเข้าในทุก URL เมื่อมีการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7f01f-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f01f-174">อย่าใช้ส่วนหัวและส่วนท้ายสากลที่มีการเชื่อมโยงที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="7f01f-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="7f01f-175">เนื่องจากหน้าเหล่านี้จะถูกโฮสต์ในโดเมน B2C Azure AD เมื่อมีการใช้งาน จะมีการใช้เฉพาะ URL สัมบูรณ์สำหรับลิงก์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7f01f-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="7f01f-176">ตั้งค่าคอนฟิกนโยบาย B2C Azure AD ด้วยข้อมูลของหน้าแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7f01f-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="7f01f-177">ในพอร์ทัล Azure ให้กลับไปที่หน้า **B2C Azure AD** แล้วบนเมนูภายใต้ **นโยบาย** ให้เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)**</span><span class="sxs-lookup"><span data-stu-id="7f01f-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="7f01f-178">อัพเดตราโยบาย "การลงทะเบียนและลงชื่อเข้าใช้" ด้วยข้อมูลของหน้าแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7f01f-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="7f01f-179">หากต้องการอัพเดตนโยบาย "การลงทะเบียนและลงชื่อเข้าใช้" ด้วยข้อมูลของหน้าแบบกำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-180">ในนโยบาย **ลงทะเบียนและลงชื่อเข้าใช้** ที่คุณตั้งค่าคอนฟิกก่อนหน้านี้ ในบานหน้าต่างนำทาง ให้เลือก **โครงร่างหน้า**</span><span class="sxs-lookup"><span data-stu-id="7f01f-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7f01f-181">เลือกโครงร่าง **หน้าการลงทะเบียนหรือลงชื่อเข้าใช้โดยรวม**</span><span class="sxs-lookup"><span data-stu-id="7f01f-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="7f01f-182">ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f01f-183">ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL แบบเต็มในการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="7f01f-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="7f01f-184">รวมคำต่อท้าย **preloadscripts=true**</span><span class="sxs-lookup"><span data-stu-id="7f01f-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f01f-185">ตัวอย่างเช่น ป้อน ``www.<my domain>.com/sign-in?preloadscripts=true``</span><span class="sxs-lookup"><span data-stu-id="7f01f-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f01f-186">ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**</span><span class="sxs-lookup"><span data-stu-id="7f01f-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f01f-187">เลือกโครงร่าง **หน้าการลงทะเบียนบัญชีเฉพาะที่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="7f01f-188">ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f01f-189">ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL แบบเต็มในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="7f01f-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="7f01f-190">รวมคำต่อท้าย **preloadscripts=true**</span><span class="sxs-lookup"><span data-stu-id="7f01f-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f01f-191">ตัวอย่างเช่น ป้อน ``www.<my domain>.com/sign-up?preloadscripts=true``</span><span class="sxs-lookup"><span data-stu-id="7f01f-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f01f-192">ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**</span><span class="sxs-lookup"><span data-stu-id="7f01f-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f01f-193">ในส่วน **แอททริบิวต์ของผู้ใช้** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="7f01f-194">สำหรับแอททริบิวต์ **ที่อยู่อีเมล** **ชื่อที่กำหนด** และ **นามสกุล** ให้เลือก **ไม่** ในฟิลด์ **ต้องมีการตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="7f01f-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="7f01f-195">สำหรับแอททริบิวต์ **ชื่อที่กำหนด** และ **นามสกุล** ให้เลือก **ไม่** ในฟิลด์ **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="7f01f-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![การตั้งค่าคอนฟิกของนโยบายหน้าการลงทะเบียนบัญชีภายในเครื่อง](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="7f01f-197">อัพเดตนโยบาย "การแก้ไขโพรไฟล์" ด้วยข้อมูลของหน้าแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7f01f-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="7f01f-198">หากต้องการอัพเดตนโยบาย "การแก้ไขโพรไฟล์" ด้วยข้อมูลของหน้าแบบกำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-199">ในนโยบาย **การแก้ไขโพรไฟล์** ที่คุณตั้งค่าคอนฟิกก่อนหน้านี้ ในบานหน้าต่างนำทาง ให้เลือก **โครงร่างหน้า**</span><span class="sxs-lookup"><span data-stu-id="7f01f-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7f01f-200">เลือกโครงร่าง **หน้าแก้ไขโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="7f01f-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="7f01f-201">ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f01f-202">ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL แก้ไขโพรไฟล์แบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="7f01f-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="7f01f-203">รวมคำต่อท้าย **preloadscripts=true**</span><span class="sxs-lookup"><span data-stu-id="7f01f-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f01f-204">ตัวอย่างเช่น ป้อน ``www.<my domain>.com/profile-edit?preloadscripts=true``</span><span class="sxs-lookup"><span data-stu-id="7f01f-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f01f-205">ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**</span><span class="sxs-lookup"><span data-stu-id="7f01f-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f01f-206">ในส่วน **แอททริบิวต์ของผู้ใช้** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="7f01f-207">สำหรับแอททริบิวต์ **ที่อยู่อีเมล** **ชื่อที่กำหนด** ให้เลือก **ไม่** ในฟิลด์ **ต้องมีการตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="7f01f-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="7f01f-208">สำหรับแอททริบิวต์ **ชื่อที่กำหนด** และ **นามสกุล** ให้เลือก **ไม่** ในฟิลด์ **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="7f01f-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="7f01f-209">อัพเดตนโยบาย "การรีเซ็ตรหัสผ่าน" ด้วยข้อมูลของหน้าแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="7f01f-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="7f01f-210">หากต้องการอัพเดตนโยบาย "การรีเซ็ตรหัสผ่าน" ด้วยข้อมูลของหน้าแบบกำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="7f01f-211">ในนโยบาย **การรีเซ็ตรหัสผ่าน** ที่คุณตั้งค่าคอนฟิกก่อนหน้านี้ ในบานหน้าต่างนำทาง ให้เลือก **โครงร่างหน้า**</span><span class="sxs-lookup"><span data-stu-id="7f01f-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="7f01f-212">เลือกโครงร่าง **หน้ารหัสผ่านใหม่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="7f01f-213">ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f01f-214">ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL รีเซ็ตพาสเวิร์ดแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="7f01f-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="7f01f-215">รวมคำต่อท้าย **preloadscripts=true**</span><span class="sxs-lookup"><span data-stu-id="7f01f-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f01f-216">ตัวอย่างเช่น ป้อน ``www.<my domain>.com/passwordreset?preloadscripts=true``</span><span class="sxs-lookup"><span data-stu-id="7f01f-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f01f-217">ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**</span><span class="sxs-lookup"><span data-stu-id="7f01f-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="7f01f-218">เลือกโครงร่าง **หน้าการตรวจสอบบัญชี**</span><span class="sxs-lookup"><span data-stu-id="7f01f-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="7f01f-219">ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="7f01f-220">ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL การตรวจสอบความถูกต้องของการรีเซ็ตรหัสผ่านแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="7f01f-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="7f01f-221">รวมคำต่อท้าย **preloadscripts=true**</span><span class="sxs-lookup"><span data-stu-id="7f01f-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="7f01f-222">ตัวอย่างเช่น ป้อน ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``</span><span class="sxs-lookup"><span data-stu-id="7f01f-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="7f01f-223">ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**</span><span class="sxs-lookup"><span data-stu-id="7f01f-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="7f01f-224">ปรับแต่งสตริงข้อความเริ่มต้นสำหรับป้ายชื่อและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="7f01f-225">ในไลบรารีโมดูล การลงชื่อเข้าใช้ในโมดูลจะมีการกรอกข้อมูลล่วงหน้ากับสตริงข้อความเริ่มต้นสำหรับป้ายชื่อและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7f01f-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="7f01f-226">คุณสามารถเลือกกำหนดสตริงเหล่านี้ในชุดการพัฒนาซอฟต์แวร์ (SDK) โดยอัพเดตค่าในไฟล์ global.json สากลสำหรับลงชื่อเข้าใช้ในโมดูล</span><span class="sxs-lookup"><span data-stu-id="7f01f-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="7f01f-227">ตัวอย่างเช่นข้อความเริ่มต้นสำหรับลิงก์ลืมรหัสผ่าน คือ **ลืมรหัสผ่านใช่หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="7f01f-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="7f01f-228">ต่อไปนี้เป็นการแสดงข้อความเริ่มต้นนี้บนหน้าการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="7f01f-228">The following shows this default text on the sign-in page.</span></span>

![ข้อความเริ่มต้นสำหรับลิงก์รหัสผ่านที่ลืมบนหน้าลงชื่อเข้าใช้](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="7f01f-230">อย่างไรก็ตาม ในไฟล์ global.json สำหรับโมดูลการลงชื่อเข้าใช้ในไลบรารีโมดูล คุณสามารถแก้ไขข้อความเป็น **ลืมรหัสผ่านใช่หรือไม่** ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7f01f-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![ข้อความลิงก์ที่อัพเดตในการลงชื่อเข้าใช้ในโมดูลไฟล์ global.json](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="7f01f-232">หลังจากที่คุณอัปเดตไฟล์ global.json และเผยแพร่การเปลี่ยนแปลงของคุณ ข้อความลิงก์ใหม่จะปรากฏขึ้นในโมดูลการลงชื่อเข้าใช้ ทั้งใน Commerce และบนหน้าลงชื่อเข้าใช้แบบใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="7f01f-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f01f-233">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7f01f-233">Additional resources</span></span>

[<span data-ttu-id="7f01f-234">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f01f-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7f01f-235">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="7f01f-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7f01f-236">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="7f01f-236">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7f01f-237">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="7f01f-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7f01f-238">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="7f01f-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7f01f-239">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="7f01f-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7f01f-240">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="7f01f-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7f01f-241">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="7f01f-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7f01f-242">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="7f01f-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7f01f-243">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="7f01f-243">Enable location-based store detection</span></span>](enable-store-detection.md)
