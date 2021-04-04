---
title: ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce
description: หัวข้อนี้จะอธิบายเกี่ยวกับเวลาและวิธีการตั้งค่าผู้เช่าธุรกิจ-ผู้บริโภค (B2C) ของ Microsoft Azure Active Directory (Azure AD) แบบหลายรายการต่อหนึ่งช่องทาง สำหรับการตรวจสอบความถูกต้องของผู้ใช้ในสภาพแวดล้อม Dynamics 365 Commerce เฉพาะ
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ddc8cea42ab0b5a319d4725ce8c75e57529cc63
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477767"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="389cb-103">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="389cb-104">หัวข้อนี้จะอธิบายเกี่ยวกับเวลาและวิธีการตั้งค่าผู้เช่าธุรกิจ-ผู้บริโภค (B2C) ของ Microsoft Azure Active Directory (Azure AD) ต่อหนึ่งช่องทาง สำหรับการตรวจสอบความถูกต้องของผู้ใช้ในสภาพแวดล้อม Dynamics 365 Commerce เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="389cb-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="389cb-105">Dynamics 365 Commerce ใช้บริการตัวระบุข้อมูลเฉพาะตัวระบบคลาวด์ของ Azure AD B2C เพื่อสนับสนุนข้อมูลประจำตัวของผู้ใช้และขั้นตอนการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="389cb-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="389cb-106">ผู้ใช้สามารถใช้ขั้นตอนการรับรองความถูกต้องในการลงชื่อสมัคร ลงชื่อเข้าใช้ และรีเซ็ตรหัสผ่านของตน</span><span class="sxs-lookup"><span data-stu-id="389cb-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="389cb-107">Azure AD B2C จัดเก็บข้อมูลการตรวจสอบความถูกต้องที่สำคัญของผู้ใช้ เช่น ชื่อผู้ใช้และรหัสผ่านของเขาหรือเธอ</span><span class="sxs-lookup"><span data-stu-id="389cb-107">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="389cb-108">เรกคอร์ดผู้ใช้ไม่ซ้ำกันสำหรับผู้เช่า B2C แต่ละราย และใช้ข้อมูลส่วนบุคคลของชื่อผู้ใช้ (ที่อยู่อีเมล) หรือข้อมูลส่วนบุคคลของผู้ให้บริการข้อมูลประจำตัวทางสังคม</span><span class="sxs-lookup"><span data-stu-id="389cb-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="389cb-109">ในกรณีส่วนใหญ่ ผู้เช่า Azure AD B2C เดียวจะถูกใช้ในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="389cb-110">ลูกค้า Commerce สามารถสร้างและเผยแพร่ไซต์หลายไซต์ในสภาพแวดล้อม Commerce เดียวกัน และจะมีการใช้ข้อมูลประจำตัวของลูกค้ารายเดียวกันในไซต์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="389cb-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="389cb-111">อย่างไรก็ตาม ถ้าไซต์ในสภาพแวดล้อมควรได้รับการปฏิบัติเช่นเดียวกับแบรนด์ต่างๆ และปรากฏให้ผู้ใช้เป็นธุรกิจแยกต่างหาก ผู้เช่า B2C สามารถถูกตั้งค่าคอนฟิกสำหรับช่องทางที่ใช้สำหรับการแยกไซต์/แบรนด์</span><span class="sxs-lookup"><span data-stu-id="389cb-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="389cb-112">ข้อควรพิจารณาเมื่อมีการตั้งค่าผู้เช่า B2C หลายรายการสำหรับแต่ละช่องทาง</span><span class="sxs-lookup"><span data-stu-id="389cb-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="389cb-113">บ่อยครั้ง เมื่อช่องทางหรือไซต์แต่ละแห่งได้รับการจัดการเป็นธุรกิจแยกต่างหาก ตัวเลือกที่ดีที่สุดโดยอ้างอิงขั้นตอนการตรวจสอบความถูกต้องของผู้ใช้ใน Commerce คือการใช้นิติบุคคลแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="389cb-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="389cb-114">อย่างไรก็ตาม ถ้าคุณต้องการเก็บแต่ละช่องทาง/ไซต์ในสภาพแวดล้อมและนิติบุคคลเดียวกัน แต่ต้องการให้มีการตรวจสอบความถูกต้องของผู้ใช้แยกต่างหากสำหรับแต่ละไซต์ คุณควรพิจารณาจุดต่อไปนี้ก่อนที่คุณจะดำเนินการต่อ:</span><span class="sxs-lookup"><span data-stu-id="389cb-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="389cb-115">ผู้ใช้จะมีข้อมูลประจำตัวที่ไม่ซ้ำกันของตนเองสำหรับแต่ละช่องทาง/ไซต์</span><span class="sxs-lookup"><span data-stu-id="389cb-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="389cb-116">บุคคลเดียวกันสามารถมีบัญชีแยกต่างหากสองบัญชีต่อช่องสัญญาณ/ไซต์ เนื่องจากบัญชีแต่ละบัญชีจะเป็นรายการเฉพาะในผู้เช่า B2C ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="389cb-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="389cb-117">ในสภาพแวดล้อม Microsoft Dynamics เรกคอร์ดลูกค้าแยกต่างหากจะถูกส่งคืนสำหรับการค้นหาเรกคอร์ดสากล</span><span class="sxs-lookup"><span data-stu-id="389cb-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="389cb-118">ถ้าผู้ใช้ใช้ที่อยู่อีเมลเดียวกันระหว่างช่องทาง/ไซต์ การค้นหาลูกค้าสากลจะส่งคืนผลลัพธ์สำหรับแต่ละช่องทาง/ไซต์</span><span class="sxs-lookup"><span data-stu-id="389cb-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="389cb-119">(ตัวบ่งชี้ช่องสัญญาณจะแสดงขึ้น)</span><span class="sxs-lookup"><span data-stu-id="389cb-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="389cb-120">สมุดที่อยู่สามารถใช้เพื่อช่วยในการจัดกลุ่มผู้ใช้ เพื่อให้สามารถติดตามพวกเขาได้สำหรับแต่ละช่องทาง</span><span class="sxs-lookup"><span data-stu-id="389cb-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="389cb-121">จำนวนเรกคอร์ดลูกค้าสำหรับแต่ละช่องสัญญาณอาจเพิ่มขึ้น และการเพิ่มขึ้นนี้อาจส่งผลกระทบต่อประสิทธิภาพการทำงานของการค้นหาลูกค้าสากล</span><span class="sxs-lookup"><span data-stu-id="389cb-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="389cb-122">ผู้เช่า B2C ต้องถูกแม็ปไปยังช่องทางอย่างระมัดระวัง เพื่อช่วยป้องกันสถานการณ์ที่ลูกค้าลงชื่อสมัครสำหรับผู้เช่าที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="389cb-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="389cb-123">มิฉะนั้น ความสับสนหรือปัญหาในการติดตามอาจเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="389cb-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="389cb-124">ภาพประกอบต่อไปนี้แสดงผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![ผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](media/MultiB2C_In_Environment.png)

<span data-ttu-id="389cb-126">ถ้าคุณตัดสินใจว่าธุรกิจของคุณต้องการผู้เช่า B2C เฉพาะสำหรับแต่ละช่องทางในสภาพแวดล้อม Commerce เดียวกัน ให้ทำตามกระบวนงานในส่วนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อร้องขอลักษณะการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="389cb-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="389cb-127">ร้องขอ B2C สำหรับแต่ละช่องทางให้ถูกเปิดใช้งานในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="389cb-127">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="389cb-128">ในขณะนี้ ถ้าคุณต้องการให้ผู้เช่า B2C ที่แตกต่างกันสำหรับแต่ละช่องทางให้พร้อมใช้งานในสภาพแวดล้อม Commerce เดียวกันคุณต้องส่งคำขอไปยัง Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-128">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="389cb-129">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ได้รับการสนับสนุนสำหรับ Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) หรือหารือเกี่ยวกับปัญหานี้กับผู้ติดต่อโซลูชัน Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="389cb-129">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="389cb-130">ตั้งค่าคอนฟิกผู้เช่า B2C ในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="389cb-130">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="389cb-131">หากต้องการตั้งค่าคอนฟิกผู้เช่า B2C ในสภาพแวดล้อมของคุณ ให้ดำเนินการกระบวนงานที่เกี่ยวข้องในส่วนนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="389cb-131">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="389cb-132">เพิ่มผู้เช่า Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="389cb-132">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="389cb-133">เมื่อต้องการเพิ่มผู้เช่า Azure AD B2C ให้กับสภาพแวดล้อมของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="389cb-133">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="389cb-134">ลงชื่อเข้าใช้โปรแกรมสร้างไซต์ Commerce สำหรับสภาพแวดล้อมของคุณในฐานะผู้ดูแลระบบ หากต้องการตั้งค่าคอนฟิกผู้เช่า Azure AD B2C คุณต้องเป็นผู้ดูแลระบบสำหรับสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-134">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="389cb-135">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="389cb-135">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="389cb-136">เลือก **การตั้งค่า B2C** แล้วเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="389cb-136">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="389cb-137">เลือก **เพิ่มแอพลิเคชัน B2C** และจากนั้น ป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="389cb-137">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="389cb-138">**ชื่อแอพลิเคชัน**: ให้ป้อนชื่อที่ควรใช้สำหรับแอพลิเคชันในบริบทของการจัดการใน Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-138">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="389cb-139">เราขอแนะนำให้คุณใช้ชื่อของแอพลิเคชันที่คุณเลือก เมื่อคุณตั้งค่าแอพลิเคชัน Azure AD B2C ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="389cb-139">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="389cb-140">ด้วยวิธีนี้ คุณสามารถช่วยลดความสับสน เมื่อคุณจัดการผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-140">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="389cb-141">**ชื่อผูเชา**: ให้ป้อนชื่อผู้เช่า B2C ตามที่ปรากฏในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="389cb-141">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="389cb-142">**รหัสนโยบายของการลืมรหัสผ่าน**: ป้อนรหัสนโยบาย (ชื่อของนโยบายในพอร์ทัล Azure)</span><span class="sxs-lookup"><span data-stu-id="389cb-142">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="389cb-143">**รหัสนโยบายของการลงทะเบียนและการลงชื่อเข้าใช้**: ป้อนรหัสนโยบาย (ชื่อของนโยบายในพอร์ทัล Azure)</span><span class="sxs-lookup"><span data-stu-id="389cb-143">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="389cb-144">**GUID ของไคลเอนต์**: ให้ป้อนรหัสของผู้เช่า Azure AD B2C ตามที่ปรากฏในพอร์ทัล AZURE (ไม่ใช่รหัสแอพลิเคชันสำหรับผู้เช่า B2C)</span><span class="sxs-lookup"><span data-stu-id="389cb-144">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="389cb-145">**รหัสนโยบายของการแก้ไขโพรไฟล์**: ป้อนรหัสนโยบาย (ชื่อของนโยบายในพอร์ทัล Azure)</span><span class="sxs-lookup"><span data-stu-id="389cb-145">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="389cb-146">เมื่อคุณป้อนข้อมูลนี้เสร็จแล้ว ให้เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="389cb-146">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="389cb-147">คุณควรปล่อยให้ฟิลด์ เช่น **ขอบเขต** **รหัสนโยบายแบบไม่โต้ตอบ** **รหัสไคลเอนต์แบบไม่โต้ตอบ** **โดเมนที่กำหนดเองของรล็อกอิน** และ **รหัสนโยบายการลงชื่อสมัคร** ว่างเปล่า ยกเว้นว่าทีม Dynamics 365 Commerce จะแนะนำให้คุณตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="389cb-147">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="389cb-148">ในขณะนี้ ผู้เช่า Azure AD B2C ใหม่ของคุณควรจะปรากฏในรายการภายใต้ **จัดการแอพลิเคชัน B2C**</span><span class="sxs-lookup"><span data-stu-id="389cb-148">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="389cb-149">จัดการหรือลบผู้เช่า Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="389cb-149">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="389cb-150">ลงชื่อเข้าใช้โปรแกรมสร้างไซต์ Commerce สำหรับสภาพแวดล้อมของคุณในฐานะผู้ดูแลระบบ หากต้องการตั้งค่าคอนฟิกผู้เช่า Azure AD B2C คุณต้องเป็นผู้ดูแลระบบสำหรับสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-150">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="389cb-151">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="389cb-151">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="389cb-152">เลือก **การตั้งค่า B2C** แล้วเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="389cb-152">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="389cb-153">ถ้าต้องการแก้ไขผู้เช่า B2C ให้เลือกสัญลักษณ์ดินสอที่อยู่ข้างๆ</span><span class="sxs-lookup"><span data-stu-id="389cb-153">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="389cb-154">ถ้าต้องการลบผู้เช่า B2C ให้เลือกสัญลักษณ์ถังขยะที่อยู่ข้างๆ</span><span class="sxs-lookup"><span data-stu-id="389cb-154">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="389cb-155">เลือก **บันทึก** แล้วเลือก **เผยแพร่** เพื่อเปิดใช้งานการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="389cb-155">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="389cb-156">เมื่อมีการตั้งค่าคอนฟิกผู้เช่า B2C สำหรับไซต์ที่เริ่มใช้งานจริง/ที่เผยแพร่ ผู้ใช้อาจได้ลงชื่อสมัครโดยใช้บัญชีที่มีอยู่บนผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="389cb-156">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="389cb-157">ถ้าคุณลบผู้เช่าที่ตั้งค่าคอนฟิกไว้ในเมนู **การตั้งค่าผู้เช่า \> ผู้เช่า B2C** คุณลบการเชื่อมโยงของผู้เช่า B2C จากไซต์ที่เกี่ยวข้องกับช่องทางใดๆ ของผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="389cb-157">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="389cb-158">ในกรณีนี้ ผู้ใช้ของคุณอาจไม่สามารถลงชื่อเข้าใช้ในบัญชีของตนได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="389cb-158">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="389cb-159">ดังนั้น ใช้ความระมัดระวังอย่างมากเมื่อคุณลบผู้เช่าที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="389cb-159">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="389cb-160">เมื่อมีการลบผู้เช่าที่ตั้งค่าคอนฟิกไว้ ผู้เช่า B2C และเรกคอร์ดจะยังคงได้รับการรักษาอยู่ แต่การตั้งค่าคอนฟิกระบบ Commerce ของผู้เช่าดังกล่าวจะถูกเปลี่ยนแปลงหรือลบออก</span><span class="sxs-lookup"><span data-stu-id="389cb-160">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="389cb-161">ผู้ใช้ที่พยายามลงชื่อสมัครหรือลงชื่อเข้าใช้ไซต์ จะสร้างเรกคอร์ดบัญชีใหม่ในผู้เช่า B2C เริ่มต้นหรือที่เชื่อมโยงใหม่ ซึ่งมีการตั้งค่าคอนฟิกสำหรับช่องทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="389cb-161">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="389cb-162">ตั้งค่าคอนฟิกช่องทางของคุณกับผู้เช่า B2C</span><span class="sxs-lookup"><span data-stu-id="389cb-162">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="389cb-163">ลงชื่อเข้าใช้โปรแกรมสร้างไซต์ Commerce สำหรับสภาพแวดล้อมของคุณในฐานะผู้ดูแลระบบ หากต้องการตั้งค่าคอนฟิกผู้เช่า Azure AD B2C คุณต้องเป็นผู้ดูแลระบบสำหรับสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-163">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="389cb-164">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="389cb-164">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="389cb-165">เลือก **ช่องทาง** แล้วเลือกช่องทางที่จะตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="389cb-165">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="389cb-166">ในบานหน้าต่างคุณสมบัติทางด้านขวา ในฟิลด์ **เลือกแอพลิเคชัน B2C** เลือกผู้เช่า Azure AD B2C ที่ตั้งค่าคอนฟิกที่จะใช้สำหรับช่องทางนี้</span><span class="sxs-lookup"><span data-stu-id="389cb-166">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="389cb-167">บนแถบคำสั่ง ให้เลือก **บันทึกและเผยแพร่** เพื่อยอมรับการตั้งค่าคอนฟิกใหม่หรือที่มีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="389cb-167">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="389cb-168">ถ้าคุณเปลี่ยนแอพลิเคชัน B2C ที่กำหนดให้กับช่องทาง คุณจะลบการอ้างอิงปัจจุบันที่สร้างขึ้นสำหรับผู้ใช้ใดๆ ที่มีการลงชื่อเข้าใช้ในสภาพแวดล้อมแล้ว</span><span class="sxs-lookup"><span data-stu-id="389cb-168">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="389cb-169">ในกรณีนี้ ข้อมูลประจำตัวใดๆ ที่เชื่อมโยงกับแอพลิเคชัน B2C ที่กำหนดไว้ในปัจจุบัน จะไม่พร้อมใช้งานสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="389cb-169">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="389cb-170">ดังนั้น เปลี่ยนการตั้งค่าคอนฟิก Azure AD B2C ของช่องทาง เฉพาะเมื่อคุณกำลังตั้งค่าช่องทางเป็นครั้งแรก และไม่มีผู้ใช้ที่สามารถลงชื่อสมัครได้</span><span class="sxs-lookup"><span data-stu-id="389cb-170">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="389cb-171">มิฉะนั้น ผู้ใช้อาจต้องลงชื่อสมัครอีกครั้งเพื่อสร้างเรกคอร์ดในผู้เช่า Azure AD B2C ใหม่</span><span class="sxs-lookup"><span data-stu-id="389cb-171">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="389cb-172">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="389cb-172">Additional resources</span></span>

[<span data-ttu-id="389cb-173">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="389cb-173">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="389cb-174">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="389cb-174">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="389cb-175">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="389cb-175">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="389cb-176">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="389cb-176">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="389cb-177">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="389cb-177">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="389cb-178">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="389cb-178">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="389cb-179">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="389cb-179">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="389cb-180">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="389cb-180">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="389cb-181">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="389cb-181">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="389cb-182">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="389cb-182">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
