---
title: ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีการกำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการดูตัวอย่างของ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b17f8e9b0d8a9a62714d0073561e66642b2eaf9
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057751"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="b961d-103">ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b961d-104">หัวข้อนี้อธิบายวิธีการกำหนดค่าคุณลักษณะเสริมสำหรับสภาพแวดล้อมการดูตัวอย่างของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b961d-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="b961d-105">Prerequisites</span></span>

<span data-ttu-id="b961d-106">ถ้าคุณต้องการประเมินคุณลักษณะอีเมล์ที่เป็นธุรกรรม ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b961d-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="b961d-107">คุณมีเซิร์ฟเวอร์อีเมลที่พร้อมใช้งาน (เซิร์ฟเวอร์ Simple Mail Transfer Protocol \[SMTP\]) ซึ่งสามารถใช้งานจากการสมัครใช้งาน Microsoft Azure ที่คุณเตรียมใช้งานสภาพแวดล้อมตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b961d-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="b961d-108">คุณมีที่อยู่ของชื่อโดเมนเต็ม FQDN/IP ของเซิร์ฟเวอร์ หมายเลขพอร์ต SMTP และรายละเอียดการรับรองความถูกต้องที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b961d-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="b961d-109">ถ้าคุณต้องการประเมินคุณลักษณะการจัดการสินทรัพย์ดิจิตอลโดยการบริโภครูปภาพในช่องทาง Omni ใหม่ คุณจะต้องมีชื่อของผู้เช่าระบบการจัดการเนื้อหา (CMS) ของคุณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b961d-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="b961d-110">คำแนะนำสำหรับการค้นหาชื่อนี้มีให้ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="b961d-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="b961d-111">> > > (Q: มีคำแนะนำอยู่ที่ใด)</span><span class="sxs-lookup"><span data-stu-id="b961d-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="b961d-112">กำหนดค่าแบ็คเอนด์ของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="b961d-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="b961d-113">ค้นหา URL ที่เป็นพื้นฐานของสื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="b961d-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="b961d-114">ก่อนเสร็จสิ้นกระบวนการนี้ คุณต้องทำตามขั้นตอนใน [ตั้งค่าไซต์ของคุณใน Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce)</span><span class="sxs-lookup"><span data-stu-id="b961d-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="b961d-115">ล็อกอินเข้าสู่เครื่องมือการจัดการไซต์ Commerce โดยใช้ URL ที่คุณจดบันทึกเมื่อคุณเริ่มต้นอีคอมเมิร์ซในระหว่างการจัดเตรียม (โปรดดู [การเริ่มต้นอีคอมเมิร์ซ](provisioning-guide.md#initialize-e-commerce))</span><span class="sxs-lookup"><span data-stu-id="b961d-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="b961d-116">เปิดไซต์ **Fabrikam**</span><span class="sxs-lookup"><span data-stu-id="b961d-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="b961d-117">บนเมนูด้านซ้าย ให้เลือก **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="b961d-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="b961d-118">เลือกสินทรัพย์ที่เป็นรูปภาพรูปเดียวใด ๆ</span><span class="sxs-lookup"><span data-stu-id="b961d-118">Select any single image asset.</span></span>
1. <span data-ttu-id="b961d-119">ในตัวตรวจสอบคุณสมบัติทางด้านขวา ให้ค้นหาคุณสมบัติ **URL สาธารณะ**</span><span class="sxs-lookup"><span data-stu-id="b961d-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="b961d-120">ค่าคือ URL</span><span class="sxs-lookup"><span data-stu-id="b961d-120">The value is a URL.</span></span> <span data-ttu-id="b961d-121">นี่คือตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="b961d-121">Here is an example:</span></span>

    <span data-ttu-id="b961d-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`</span><span class="sxs-lookup"><span data-stu-id="b961d-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="b961d-123">แทนที่ตัวระบุตัวสุดท้ายใน URL (**MA1nQC** โดยใช้สตริง **search?fileName=**</span><span class="sxs-lookup"><span data-stu-id="b961d-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="b961d-124">นี่คือ URL ตัวอย่างหลังจากทำการเปลี่ยนแปลงนี้:</span><span class="sxs-lookup"><span data-stu-id="b961d-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="b961d-125">URL นี้เป็น URL ฐานสื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="b961d-125">This URL is your media base URL.</span></span> <span data-ttu-id="b961d-126">จดบันทึก</span><span class="sxs-lookup"><span data-stu-id="b961d-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="b961d-127">อัปเดต URL พื้นฐานของสื่อ</span><span class="sxs-lookup"><span data-stu-id="b961d-127">Update the media base URL</span></span>

1. <span data-ttu-id="b961d-128">ลงชื่อเข้าใช้ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-128">Sign in to Dynamics 365 Commerce.</span></span>
1. <span data-ttu-id="b961d-129">ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> โพรไฟล์ของช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="b961d-129">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="b961d-130">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b961d-130">Select **Edit**.</span></span>
1. <span data-ttu-id="b961d-131">ภายใต้ **คุณสมบัติของโพรไฟล์** ให้แทนที่ค่าคุณสมบัติสำหรับ **URL พื้นฐานของเซิร์ฟเวอร์สื่อ** ด้วย URL พื้นฐานของสื่อที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b961d-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="b961d-132">ในรายการทางด้านซ้าย ใต้ช่องทาง **เริ่มต้น** ให้เลือกช่องทางอื่น</span><span class="sxs-lookup"><span data-stu-id="b961d-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="b961d-133">ภายใต้ **คุณสมบัติของโพรไฟล์** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="b961d-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="b961d-134">สำหรับคุณสมบัติที่ถูกเพิ่ม ให้เลือก**URL ฐานของสื่อเซิร์ฟเวอร์** เป็นคีย์คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b961d-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="b961d-135">ในฐานะที่เป็นค่าคุณสมบัติ ให้ป้อน URL ฐานสื่อที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b961d-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="b961d-136">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b961d-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="b961d-137">ตั้งค่าเซิร์ฟเวอร์อีเมล</span><span class="sxs-lookup"><span data-stu-id="b961d-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="b961d-138">โปรดทราบว่าเซิร์ฟเวอร์ SMTP หรือบริการอีเมลที่คุณป้อนที่นี่ต้องสามารถเข้าถึงได้จากการสมัครใช้งาน Azure ที่คุณใช้สำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="b961d-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="b961d-139">ลงชื่อเข้าใช้ Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-139">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b961d-140">ใช้เมนูด้านซ้าย ไปที่ **โมดูล \> การจัดการระบบ \> ตั้งค่า \> อีเมล \> พารามิเตอร์อีเมล**</span><span class="sxs-lookup"><span data-stu-id="b961d-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="b961d-141">บนแท็บ **การตั้งค่า SMTP** ในฟิลด์ **เซิร์ฟเวอร์อีเมลขาออก** ให้ป้อน FQDN หรือที่อยู่ IP ของบริการของเซิร์ฟเวอร์ SMTP หรืออีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="b961d-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="b961d-142">ในฟิลด์ **หมายเลขพอร์ต SMTP** ให้ป้อนหมายเลขพอร์ต</span><span class="sxs-lookup"><span data-stu-id="b961d-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="b961d-143">(ถ้าคุณไม่ได้ใช้ Secure Sockets Layer \[SSL\] หมายเลขพอร์ตเริ่มต้นคือ **25**)</span><span class="sxs-lookup"><span data-stu-id="b961d-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="b961d-144">ถ้าจำเป็นต้องใช้การรับรอง ให้ป้อนค่าในฟิลด์ **ชื่อผู้ใช้** และ**รหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="b961d-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="b961d-145">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b961d-145">Select **Save**.</span></span>
1. <span data-ttu-id="b961d-146">เลือก**รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="b961d-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="b961d-147">บนแท็บ **การทดสอบอีเมล** ในฟิลด์ **ผู้ให้บริการอีเมล** เลือก**SMTP** </span><span class="sxs-lookup"><span data-stu-id="b961d-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="b961d-148">ในฟิลด์ **ส่งไปยัง** ให้ป้อนที่อยู่อีเมลที่คุณต้องการให้อีเมลทดสอบส่งไป</span><span class="sxs-lookup"><span data-stu-id="b961d-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="b961d-149">เลือก **ส่งอีเมลทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="b961d-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="b961d-150">ตั้งค่าเท็มเพลตของอีเมล</span><span class="sxs-lookup"><span data-stu-id="b961d-150">Configure email templates</span></span>

<span data-ttu-id="b961d-151">สำหรับแต่ละเหตุการณ์ธุรกรรมที่คุณต้องการส่งอีเมล คุณต้องอัปเดตเท็มเพลตอีเมลด้วยที่อยู่อีเมลของผู้ส่งที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b961d-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="b961d-152">ลงชื่อเข้าใช้ Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-152">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b961d-153">ใช้เมนูด้านซ้าย ไปที่ **โมดูล \> การจัดการองค์กร \> ตั้งค่า \> เท็มเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="b961d-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="b961d-154">เลือก **แสดงรายการ**</span><span class="sxs-lookup"><span data-stu-id="b961d-154">Select **Show list**.</span></span>
1. <span data-ttu-id="b961d-155">สำหรับแต่ละเท็มเพลตในรายการ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="b961d-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="b961d-156">ในฟิลด์ **อีเมลผู้ส่ง** ป้อนอยู่อีเมลของผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="b961d-157">ไม่บังคับ: ในฟิลด์ **ชื่อผู้ส่ง** ให้ป้อนชื่อที่ควรใช้เป็นชื่อผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="b961d-158">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b961d-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="b961d-159">กำหนดเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="b961d-159">Customize email templates</span></span>

<span data-ttu-id="b961d-160">คุณอาจต้องการปรับแต่งเท็มเพลตอีเมลเพื่อให้ใช้รูปภาพที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b961d-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="b961d-161">หรือคุณอาจต้องการปรับปรุงการเชื่อมโยงในเท็มเพลตเพื่อให้พวกเขาไปที่สภาพแวดล้อมการแสดงตัวอย่างของคุณ</span><span class="sxs-lookup"><span data-stu-id="b961d-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="b961d-162">กระบวนการนี้จะอธิบายวิธีการดาวน์โหลดเท็มเพลตเริ่มต้น เลือกกำหนดเท็มเพลตเหล่านั้น และอัปเดตเท็มเพลตในระบบ</span><span class="sxs-lookup"><span data-stu-id="b961d-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="b961d-163">ใช้เว็บเบราว์เซอร์ ดาวน์โหลด [ไฟล์ .zip เท็มเพลตอีเมลเริ่มต้นของ Microsoft Dynamics 365 Commerce Preview](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) ลงในคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b961d-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="b961d-164">ไฟล์นี้จะประกอบด้วยเอกสาร HTML ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b961d-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="b961d-165">เท็มเพลตการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-165">Order confirmation template</span></span>
    - <span data-ttu-id="b961d-166">เท็มเพลตการออกบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="b961d-166">Issue gift card template</span></span>
    - <span data-ttu-id="b961d-167">เท็มเพลตใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="b961d-167">New order template</span></span>
    - <span data-ttu-id="b961d-168">เท็มเพลตใบสั่งแพ็คสินค้า</span><span class="sxs-lookup"><span data-stu-id="b961d-168">Pack order template</span></span>
    - <span data-ttu-id="b961d-169">เท็มเพลตใบสั่งรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b961d-169">Pick order template</span></span>

1. <span data-ttu-id="b961d-170">เลือกกำหนดเท็มเพลตโดยใช้ตัวแก้ไขข้อความหรือ HTML</span><span class="sxs-lookup"><span data-stu-id="b961d-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="b961d-171">ดูรายการ [โทเค็นที่สนับสนุน](#supported-tokens-in-the-email-template) ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="b961d-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="b961d-172">ลงชื่อเข้าใช้ Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-172">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b961d-173">ใช้เมนูด้านซ้าย ไปที่ **โมดูล \> การจัดการองค์กร \> ตั้งค่า \> เท็มเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="b961d-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="b961d-174">ขยายรายการด้านซ้ายเพื่อดูเท็มเพลตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b961d-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="b961d-175">สำหรับแต่ละเท็มเพลตที่คุณต้องการกำหนดเอง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="b961d-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="b961d-176">เลือกเท็มเพลตในรายการ</span><span class="sxs-lookup"><span data-stu-id="b961d-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="b961d-177">ภายใต้ **เนื้อหาของข้อความอีเมล** ให้เลือกรุ่นภาษาที่เหมาะสมในรายการ</span><span class="sxs-lookup"><span data-stu-id="b961d-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="b961d-178">(ภาษาเริ่มต้นคือ **en-us**)</span><span class="sxs-lookup"><span data-stu-id="b961d-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="b961d-179">ใต้ **เนื้อหาข้อความอีเมล** ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b961d-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="b961d-180">บานหน้าต่าง**อัปโหลดเท็มเพลตอีเมล** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b961d-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="b961d-181">เลือก **เรียกดู**และค้นหาไฟล์ HTML ที่มีเนื้อหาที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b961d-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="b961d-182">เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="b961d-182">Select **Upload**.</span></span> <span data-ttu-id="b961d-183">เท็มเพลตของคุณจะถูกอัปโหลดไปยังระบบ และตัวอย่างจะแสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="b961d-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="b961d-184">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b961d-184">Select **OK**.</span></span>
    1. <span data-ttu-id="b961d-185">ไม่จำเป็น: กำหนดคุณสมบัติ **ชื่อเรื่อง** ของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="b961d-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="b961d-186">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b961d-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="b961d-187">โทเคนที่สนับสนุนในเท็มเพลตอีเมล์</span><span class="sxs-lookup"><span data-stu-id="b961d-187">Supported tokens in the email template</span></span>

<span data-ttu-id="b961d-188">เมื่ออีเมลถูกส่ง โทเคนเหล่านี้จะถูกแทนที่ด้วยค่าจริงที่ใช้กับลูกค้าและใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b961d-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="b961d-189">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="b961d-189">Sales order</span></span>

<span data-ttu-id="b961d-190">โทเคนต่อไปนี้จะใช้กับใบสั่งขายในภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b961d-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="b961d-191">ชื่อของโทเคน</span><span class="sxs-lookup"><span data-stu-id="b961d-191">Name of the token</span></span> | <span data-ttu-id="b961d-192">โทเคน</span><span class="sxs-lookup"><span data-stu-id="b961d-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="b961d-193">หมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-193">Order number</span></span>      | <span data-ttu-id="b961d-194">%salesId%</span><span class="sxs-lookup"><span data-stu-id="b961d-194">%salesid%</span></span> |
| <span data-ttu-id="b961d-195">ชื่อของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b961d-195">Customer's name</span></span>   | <span data-ttu-id="b961d-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="b961d-196">%customername%</span></span> |
| <span data-ttu-id="b961d-197">ที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-197">Delivery address</span></span>  | <span data-ttu-id="b961d-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="b961d-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="b961d-199">ที่อยู่ที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="b961d-199">Billing address</span></span>   | <span data-ttu-id="b961d-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="b961d-200">%customeraddress%</span></span> |
| <span data-ttu-id="b961d-201">วันที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-201">Order date</span></span>        | <span data-ttu-id="b961d-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="b961d-202">%shipdate%</span></span> |
| <span data-ttu-id="b961d-203">วิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-203">Delivery mode</span></span>     | <span data-ttu-id="b961d-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="b961d-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="b961d-205">ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b961d-205">Discount</span></span>          | <span data-ttu-id="b961d-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="b961d-206">%discount%</span></span> |
| <span data-ttu-id="b961d-207">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="b961d-207">Sales tax</span></span>         | <span data-ttu-id="b961d-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="b961d-208">%tax%</span></span> |
| <span data-ttu-id="b961d-209">ผลรวมของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-209">Order total</span></span>       | <span data-ttu-id="b961d-210">%total%</span><span class="sxs-lookup"><span data-stu-id="b961d-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="b961d-211">รายการขาย</span><span class="sxs-lookup"><span data-stu-id="b961d-211">Sales line</span></span>

<span data-ttu-id="b961d-212">โทเคนต่อไปนี้จะถูกแทนที่ด้วยค่าสำหรับผลิตภัณฑ์แต่ละรายการในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="b961d-213">วางโทเค็น **รายการผลิตภัณฑ์ - เริ่มต้น** ที่จุดเริ่มต้นของบล็อก HTML ที่ถูกทำซ้ำสำหรับทุกผลิตภัณฑ์ และวางโทเค็น **รายการผลิตภัณฑ์ - สิ้นสุด** ที่ส่วนท้ายของบล็อก</span><span class="sxs-lookup"><span data-stu-id="b961d-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="b961d-214">ชื่อของโทเคน</span><span class="sxs-lookup"><span data-stu-id="b961d-214">Name of the token</span></span>      | <span data-ttu-id="b961d-215">โทเคน</span><span class="sxs-lookup"><span data-stu-id="b961d-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="b961d-216">รายการผลิตภัณฑ์ - เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b961d-216">Product list - start</span></span>   | <span data-ttu-id="b961d-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="b961d-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="b961d-218">รายการผลิตภัณฑ์ - สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="b961d-218">Product list - end</span></span>     | <span data-ttu-id="b961d-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="b961d-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="b961d-220">ชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b961d-220">Product name</span></span>           | <span data-ttu-id="b961d-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="b961d-221">%lineproductname%</span></span> |
| <span data-ttu-id="b961d-222">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b961d-222">Description</span></span>            | <span data-ttu-id="b961d-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="b961d-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="b961d-224">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="b961d-224">Quantity</span></span>               | <span data-ttu-id="b961d-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="b961d-225">%linequantity%</span></span> |
| <span data-ttu-id="b961d-226">ราคาต่อหน่วยในรายการ</span><span class="sxs-lookup"><span data-stu-id="b961d-226">Line unit price</span></span>        | <span data-ttu-id="b961d-227">% lineprice% (ตรวจสอบ)</span><span class="sxs-lookup"><span data-stu-id="b961d-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="b961d-228">จำนวนสินค้าทั้งหมดในรายการ</span><span class="sxs-lookup"><span data-stu-id="b961d-228">line item total</span></span>        | <span data-ttu-id="b961d-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="b961d-229">%linenetamount%</span></span> |
| <span data-ttu-id="b961d-230">line discount / ส่วนลดต่อรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="b961d-230">line discount</span></span>          | <span data-ttu-id="b961d-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="b961d-231">%linediscount%</span></span> |
| <span data-ttu-id="b961d-232">วันที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-232">Ship date</span></span>              | <span data-ttu-id="b961d-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="b961d-233">%lineshipdate%</span></span> |
| <span data-ttu-id="b961d-234">วิธีการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="b961d-234">Procurement method</span></span>     | <span data-ttu-id="b961d-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="b961d-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="b961d-236">delivery address / ที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b961d-236">delivery address</span></span>       | <span data-ttu-id="b961d-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="b961d-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="b961d-238">หน่วยการขายของรายการ</span><span class="sxs-lookup"><span data-stu-id="b961d-238">Sales unit of the line</span></span> | <span data-ttu-id="b961d-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="b961d-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b961d-240">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b961d-240">Additional resources</span></span>

[<span data-ttu-id="b961d-241">ภาพรวมของสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b961d-242">เตรียมใช้งานสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b961d-243">ตั้งค่าคอนฟิกสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b961d-244">FAQ เกี่ยวกับสภาพแวดล้อมการแสดงตัวอย่างของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b961d-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b961d-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b961d-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b961d-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b961d-247">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="b961d-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b961d-248">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b961d-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
