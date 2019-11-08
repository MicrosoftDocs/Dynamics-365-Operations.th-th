---
title: ตั้งค่าคอนฟิกการตั้งค่าอีเมลใน Microsoft Dynamics 365 Talent - Attract
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลที่ส่งโดย Microsoft Dynamcis 365 Talent - Attract
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a457deec757a5d5a3e01c6903b2dd7a9d975ef0b
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551552"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="5ef04-103">ตั้งค่าคอนฟิกการตั้งค่าอีเมลใน Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="5ef04-103">Configure email settings in Microsoft Dynamics 365 Talent - Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5ef04-104">แบรนด์ของคุณสร้างความไว้วางใจและช่วยคุณในการสร้างความสัมพันธ์กับผู้สมัคร ก่อนที่พวกเขาจะสมัครตำแหน่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="5ef04-105">การรับรู้แบรนด์ในเชิงบวกดึงดูด talent สูงสุด และเพิ่มความภักดีของพนักงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5ef04-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="5ef04-106">Microsoft Dynamics 365 Talent: Attract: ให้คุณตั้งค่าคอนฟิกอีเมล เพื่อให้สะท้อนถึงแบรนด์ของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="5ef04-107">ดังนั้น คุณจึงสามารถให้ประสบการณ์ที่สอดคล้องกับผู้สมัครงานได้ เนื่องจากทำการดำเนินการผ่านกระบวนการแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="5ef04-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="5ef04-108">Attract อนุญาตให้คุณทำการดำเนินการเหล่านี้ได้:</span><span class="sxs-lookup"><span data-stu-id="5ef04-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="5ef04-109">ตั้งค่าคอนฟิกการตั้งค่าอีเมล เพื่อให้มีการใช้บัญชีบริการอีเมลของ Microsoft Exchange ของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="5ef04-110">ในลักษณะนี้ ผู้สมัครทราบว่าอีเมลมาจากบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="5ef04-111">ตัวอย่างเช่น คุณสามารถตั้งค่าคอนฟิกการตั้งค่าของคุณ เพื่อให้ผู้สมัครได้รับอีเมลจาก `recruiting@contoso.com` แทน `contoso@microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="5ef04-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="5ef04-112">สร้างการสร้างแบรนด์ที่สอดคล้องสำหรับการสื่อสารทางอีเมลของคุณทั้งหมด โดยการตั้งค่าส่วนหัวและส่วนท้ายส่วนกลางสำหรับเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ef04-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ef04-113">เมื่อต้องการตั้งค่าคอนฟิก Attract เพื่อให้ใช้บัญชีบริการอีเมลของบริษัทของคุณในการส่งอีเมล คุณต้องมี add-on ของการจ้างงานที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="5ef04-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="5ef04-114">เชื่อมต่อบัญชีบริการอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ef04-114">Connect an email service account</span></span>

<span data-ttu-id="5ef04-115">โดยการเชื่อมต่อบัญชีบริการอีเมลของบริษัทของคุณ คุณสามารถสร้างประสบการณ์อีเมลที่มีแบรนด์สำหรับผู้สมัครงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="5ef04-116">ถ้าคุณไม่ได้เชื่อมต่อบัญชีบริษัทของคุณ Attract จะใช้บัญชีบริการอีเมลที่มีแบรนด์ของ Microsoft เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5ef04-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="5ef04-117">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมขวาบน) และจากนั้น เลือก **ศูนย์การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="5ef04-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="5ef04-118">บนแท็บ **การตั้งค่าอีเมล** ภายใต้ **บัญชีบริการอีเมล** ให้เลือก **เชื่อมต่อบัญชีบริษัท**</span><span class="sxs-lookup"><span data-stu-id="5ef04-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![การเชื่อมต่อบัญชีบริการอีเมลของบริษัทของคุณใน Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="5ef04-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างบัญชีอีเมลที่ใช้ร่วมกัน โปรดดู [กล่องจดหมายที่ใช้ร่วมกันใน Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)</span><span class="sxs-lookup"><span data-stu-id="5ef04-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="5ef04-121">ในหน้าต่างการลงชื่อเข้าใช้ Microsoft ให้เข้าสู่ระบบโดยใช้ข้อมูลประจำตัวขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="5ef04-122">ถ้าคุณยังไม่ได้ตั้งค่าบัญชีบริการอีเมล หรือถ้าคุณต้องการเพิ่มบัญชีใหม่ ให้เลือก **เพิ่มบัญชีบริการใหม่** แล้วป้อนข้อมูลอีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="5ef04-123">ถ้าคุณได้ตั้งค่าบัญชีบริการอีเมลที่คุณต้องการใช้แล้ว ให้เลือกบัญชีนั้น</span><span class="sxs-lookup"><span data-stu-id="5ef04-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="5ef04-124">เมื่อมีการตั้งค่าคอนฟิกบัญชีบริการอีเมลของคุณเสร็จเรียบร้อยแล้ว คุณจะเห็นการแสดงรายการภายใต้ **บัญชีบริการอีเมล**</span><span class="sxs-lookup"><span data-stu-id="5ef04-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="5ef04-125">ยกเลิกการเชื่อมต่อบัญชีบริการอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ef04-125">Disconnect an email service account</span></span>

<span data-ttu-id="5ef04-126">ถ้าคุณต้องการหยุดใช้โดเมนของบริษัทของคุณในการสื่อสารทางอีเมลผ่าน Attract คุณสามารถยกเลิกการเชื่อมต่อบัญชีบริการอีเมลได้</span><span class="sxs-lookup"><span data-stu-id="5ef04-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="5ef04-127">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมขวาบน) และจากนั้น เลือก **ศูนย์การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="5ef04-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="5ef04-128">บนแท็บ **การตั้งค่าอีเมล** ภายใต้ **บัญชีบริการอีเมล** เลือกปุ่ม **เพิ่มเติม** (จุดแนวตั้งสามจุด) ถัดจากบัญชีบริการอีเมลที่คุณต้องการยกเลิกการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="5ef04-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="5ef04-129">เลือก **ยกเลิกการเชื่อมต่อบัญชีอีเมล**</span><span class="sxs-lookup"><span data-stu-id="5ef04-129">Select **Disconnect email account**.</span></span>

    ![การยกเลิกการเชื่อมต่อบัญชีบริการอีเมลของบริษัทของคุณ](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="5ef04-131">เมื่อคุณได้รับพร้อมท์ให้ยืนยันการดำเนินงาน ให้เลือก **ยกเลิกการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="5ef04-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![การยืนยันการยกเลิกการเชื่อมต่อของบัญชีบริการอีเมลของบริษัทของคุณ](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="5ef04-133">ถ้าคุณไม่ได้เชื่อมต่อบัญชีบริการอีเมลอื่น อีเมลที่ถูกส่งจาก Attract จะใช้บัญชีบริการอีเมลที่มีแบรนด์ของ Microsoft เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5ef04-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="5ef04-134">ตั้งค่าคอนฟิกการตั้งค่าเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ef04-134">Configure email template settings</span></span>

<span data-ttu-id="5ef04-135">คุณสามารถอัพโหลดรูปภาพโลโก้ของบริษัทของคุณและข้อมูลอื่นๆ เป็นส่วนหัวที่มีแบรนด์สำหรับอีเมลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5ef04-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="5ef04-136">นอกจากนี้ คุณยังสามารถให้ลิงค์ไปยังนโยบายความเป็นส่วนตัวและข้อกำหนดการใช้งานของคุณในส่วนท้ายอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ef04-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef04-137">คุณต้องปฏิบัติตามกฎหมายที่เกี่ยวข้องของประเทศหรือภูมิภาคของคุณ และรวมทั้งประเทศหรือภูมิภาคที่ควบคุมดูแลผู้รับอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ef04-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="5ef04-138">กฎหมายเหล่านี้รวมถึงกฎระเบียบการป้องกันสแปม</span><span class="sxs-lookup"><span data-stu-id="5ef04-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="5ef04-139">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมขวาบน) และจากนั้น เลือก **ศูนย์การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="5ef04-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="5ef04-140">บนแท็บ **การตั้งค่าอีเมล** ภายใต้ **การตั้งค่าเท็มเพลตอีเมล** ให้ลากรูปภาพที่คุณต้องการใช้เป็นส่วนหัวของอีเมลของคุณในกล่องรูปภาพ หรือคลิกในกล่องรูปภาพเพื่อเรียกดูไฟล์</span><span class="sxs-lookup"><span data-stu-id="5ef04-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="5ef04-141">เมื่อต้องการเปลี่ยนรูปภาพที่มีอยู่ อันดับแรกคุณต้องเลือก **ลบ** ที่อยู่ถัดไป</span><span class="sxs-lookup"><span data-stu-id="5ef04-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="5ef04-142">รูปภาพต้องเป็นไฟล์ JPEG JPG PNG หรือ SVG</span><span class="sxs-lookup"><span data-stu-id="5ef04-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="5ef04-143">ขนาดที่แนะนำสำหรับรูปภาพคือ ความกว้างระหว่าง 25 และ 800 พิกเซล และความสูงระหว่าง 25 และ 150 พิกเซล</span><span class="sxs-lookup"><span data-stu-id="5ef04-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="5ef04-144">ขนาดไฟล์สูงสุดสำหรับส่วนหัวคือ1เมกะไบต์ (MB)</span><span class="sxs-lookup"><span data-stu-id="5ef04-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![การเพิ่มรูปภาพสำหรับส่วนหัวของอีเมลของบริษัทของคุณ](./media/attract-admin-email-header.png)

3. <span data-ttu-id="5ef04-146">ภายใต้ **นโยบายความเป็นส่วนตัวของคุณสำหรับการสื่อสาร** ให้ระบุลิงค์ไปยังนโยบายความเป็นส่วนตัวของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="5ef04-147">ภายใต้ **ข้อกำหนดและเงื่อนไขของคุณสำหรับการสื่อสาร** ให้ระบุลิงค์ไปยังข้อตกลงการใช้งานของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![การเพิ่มลิงค์ไปยังนโยบายความเป็นส่วนตัวและข้อกำหนดการใช้งานของบริษัทของคุณสำหรับส่วนท้ายของอีเมล](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="5ef04-149">เลือก **บันทึก** เพื่อบันทึกการตั้งค่าเท็มเพลตอีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ef04-149">Select **Save** to save your email template settings.</span></span>
