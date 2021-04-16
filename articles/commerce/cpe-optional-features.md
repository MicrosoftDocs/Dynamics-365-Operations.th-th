---
title: ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795918"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="fc083-103">ตั้งค่าคอนฟิกคุณลักษณะเสริมให้กับสภาพแวดล้อมการประเมิน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc083-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fc083-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fc083-105">Prerequisites</span></span>

<span data-ttu-id="fc083-106">ถ้าคุณต้องการประเมินคุณลักษณะอีเมล์ที่เป็นธุรกรรม ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fc083-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="fc083-107">คุณมีเซิร์ฟเวอร์อีเมลที่พร้อมใช้งาน (เซิร์ฟเวอร์ Simple Mail Transfer Protocol \[SMTP\]) ซึ่งสามารถใช้ได้จากการสมัครใช้งาน Microsoft Azure ที่ซึ่งคุณเตรียมใช้งานสภาพแวดล้อมการประเมิน</span><span class="sxs-lookup"><span data-stu-id="fc083-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="fc083-108">คุณมีที่อยู่ของชื่อโดเมนเต็ม FQDN/IP ของเซิร์ฟเวอร์ หมายเลขพอร์ต SMTP และรายละเอียดการรับรองความถูกต้องที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fc083-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="fc083-109">กำหนดค่าแบ็คเอนด์ของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="fc083-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="fc083-110">ค้นหา URL ที่เป็นพื้นฐานของสื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc083-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="fc083-111">ก่อนเสร็จสิ้นกระบวนการนี้ คุณต้องทำตามขั้นตอนใน [ตั้งค่าไซต์ของคุณใน Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce)</span><span class="sxs-lookup"><span data-stu-id="fc083-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="fc083-112">ลงชื่อเข้าใช้ตัวสร้างไซต์ Commerce โดยใช้ URL ที่คุณจดบันทึกเวลาที่คุณเริ่มต้นอีคอมเมิร์ซในระหว่างการจัดเตรียม (โปรดดู [เริ่มต้นอีคอมเมิร์ซ](provisioning-guide.md#initialize-e-commerce))</span><span class="sxs-lookup"><span data-stu-id="fc083-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="fc083-113">เปิดไซต์ **Fabrikam**</span><span class="sxs-lookup"><span data-stu-id="fc083-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="fc083-114">บนเมนูด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="fc083-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="fc083-115">เลือกสินทรัพย์ที่เป็นรูปภาพรูปเดียวใด ๆ</span><span class="sxs-lookup"><span data-stu-id="fc083-115">Select any single image asset.</span></span>
1. <span data-ttu-id="fc083-116">ในตัวตรวจสอบคุณสมบัติทางด้านขวา ให้ค้นหาคุณสมบัติ **URL สาธารณะ**</span><span class="sxs-lookup"><span data-stu-id="fc083-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="fc083-117">ค่าคือ URL</span><span class="sxs-lookup"><span data-stu-id="fc083-117">The value is a URL.</span></span> <span data-ttu-id="fc083-118">นี่คือตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="fc083-118">Here is an example:</span></span>

    <span data-ttu-id="fc083-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`</span><span class="sxs-lookup"><span data-stu-id="fc083-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="fc083-120">แทนที่ตัวระบุตัวสุดท้ายใน URL (**MA1nQC** โดยใช้สตริง) **search?fileName=**</span><span class="sxs-lookup"><span data-stu-id="fc083-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="fc083-121">นี่คือ URL ตัวอย่างหลังจากทำการเปลี่ยนแปลงนี้:</span><span class="sxs-lookup"><span data-stu-id="fc083-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="fc083-122">URL นี้เป็น URL ฐานสื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc083-122">This URL is your media base URL.</span></span> <span data-ttu-id="fc083-123">จดบันทึก</span><span class="sxs-lookup"><span data-stu-id="fc083-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="fc083-124">อัปเดต URL พื้นฐานของสื่อ</span><span class="sxs-lookup"><span data-stu-id="fc083-124">Update the media base URL</span></span>

1. <span data-ttu-id="fc083-125">ลงชื่อเข้าใช้ศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="fc083-126">ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> โพรไฟล์ของช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="fc083-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="fc083-127">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="fc083-127">Select **Edit**.</span></span>
1. <span data-ttu-id="fc083-128">ภายใต้ **คุณสมบัติของโพรไฟล์** ให้แทนที่ค่าคุณสมบัติสำหรับ **URL พื้นฐานของเซิร์ฟเวอร์สื่อ** ด้วย URL พื้นฐานของสื่อที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="fc083-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="fc083-129">เลือกช่องทางที่ชื่อ **scXXXXXXXXX**</span><span class="sxs-lookup"><span data-stu-id="fc083-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="fc083-130">ภายใต้ **คุณสมบัติของโพรไฟล์** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="fc083-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="fc083-131">สำหรับคุณสมบัติที่ถูกเพิ่ม ให้เลือก **URL ฐานของสื่อเซิร์ฟเวอร์** เป็นคีย์คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="fc083-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="fc083-132">ในฐานะที่เป็นค่าคุณสมบัติ ให้ป้อน URL ฐานสื่อที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="fc083-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="fc083-133">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fc083-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="fc083-134">ตั้งค่าคอนฟิกและทดสอบเซิร์ฟเวอร์อีเมล</span><span class="sxs-lookup"><span data-stu-id="fc083-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="fc083-135">โปรดทราบว่าเซิร์ฟเวอร์ SMTP หรือบริการอีเมลที่คุณป้อนที่นี่ต้องสามารถเข้าถึงได้จากการสมัครใช้งาน Azure ที่คุณใช้สำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="fc083-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="fc083-136">ลงชื่อเข้าใช้ศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="fc083-137">ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ของอีเมล**</span><span class="sxs-lookup"><span data-stu-id="fc083-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="fc083-138">บนแท็บ **การตั้งค่า SMTP** ในฟิลด์ **เซิร์ฟเวอร์อีเมลขาออก** ให้ป้อน FQDN หรือที่อยู่ IP ของบริการของเซิร์ฟเวอร์ SMTP หรืออีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc083-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="fc083-139">ในฟิลด์ **หมายเลขพอร์ต SMTP** ให้ป้อนหมายเลขพอร์ต</span><span class="sxs-lookup"><span data-stu-id="fc083-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="fc083-140">(ถ้าคุณไม่ได้ใช้ Secure Sockets Layer \[SSL\] หมายเลขพอร์ตเริ่มต้นคือ **25**)</span><span class="sxs-lookup"><span data-stu-id="fc083-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="fc083-141">ถ้าจำเป็นต้องใช้การรับรอง ให้ป้อนค่าในฟิลด์ **ชื่อผู้ใช้** และ **รหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="fc083-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="fc083-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fc083-142">Select **Save**.</span></span>
1. <span data-ttu-id="fc083-143">เลือก **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="fc083-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="fc083-144">บนแท็บ **การทดสอบอีเมล** ในฟิลด์ **ผู้ให้บริการอีเมล** เลือก **SMTP** </span><span class="sxs-lookup"><span data-stu-id="fc083-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="fc083-145">ในฟิลด์ **ส่งไปยัง** ให้ป้อนที่อยู่อีเมลที่คุณต้องการให้อีเมลทดสอบส่งไป</span><span class="sxs-lookup"><span data-stu-id="fc083-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="fc083-146">เลือก **ส่งอีเมลทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="fc083-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="fc083-147">ตั้งค่าเท็มเพลตของอีเมล</span><span class="sxs-lookup"><span data-stu-id="fc083-147">Configure email templates</span></span>

<span data-ttu-id="fc083-148">สำหรับแต่ละเหตุการณ์ธุรกรรมที่คุณต้องการส่งอีเมล คุณต้องอัปเดตเท็มเพลตอีเมลด้วยที่อยู่อีเมลของผู้ส่งที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fc083-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="fc083-149">ลงชื่อเข้าใช้ศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="fc083-150">ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> เท็มเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="fc083-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="fc083-151">เลือก **แสดงรายการ**</span><span class="sxs-lookup"><span data-stu-id="fc083-151">Select **Show list**.</span></span>
1. <span data-ttu-id="fc083-152">สำหรับแต่ละเท็มเพลตในรายการ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="fc083-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="fc083-153">ในฟิลด์ **อีเมลผู้ส่ง** ป้อนอยู่อีเมลของผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="fc083-154">ไม่บังคับ: ในฟิลด์ **ชื่อผู้ส่ง** ให้ป้อนชื่อที่ควรใช้เป็นชื่อผู้ส่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="fc083-155">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fc083-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="fc083-156">กำหนดเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="fc083-156">Customize email templates</span></span>

<span data-ttu-id="fc083-157">คุณอาจต้องการปรับแต่งเท็มเพลตอีเมลเพื่อให้ใช้รูปภาพที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="fc083-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="fc083-158">หรือคุณอาจต้องการปรับปรุงการเชื่อมโยงในเท็มเพลตเพื่อให้ไปที่สภาพแวดล้อมการประเมินของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc083-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="fc083-159">กระบวนการนี้จะอธิบายวิธีการดาวน์โหลดเท็มเพลตเริ่มต้น เลือกกำหนดเท็มเพลตเหล่านั้น และอัปเดตเท็มเพลตในระบบ</span><span class="sxs-lookup"><span data-stu-id="fc083-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="fc083-160">ในเว็บเบราว์เซอร์ ดาวน์โหลด [ไฟล์ .zip เท็มเพลตอีเมลเริ่มต้นของการประเมินผล Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) ลงในคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc083-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="fc083-161">ไฟล์นี้จะประกอบด้วยเอกสาร HTML ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fc083-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="fc083-162">เท็มเพลตการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-162">Order confirmation template</span></span>
    - <span data-ttu-id="fc083-163">เท็มเพลตการออกบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="fc083-163">Issue gift card template</span></span>
    - <span data-ttu-id="fc083-164">เท็มเพลตใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="fc083-164">New order template</span></span>
    - <span data-ttu-id="fc083-165">เท็มเพลตใบสั่งแพ็คสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc083-165">Pack order template</span></span>
    - <span data-ttu-id="fc083-166">เท็มเพลตใบสั่งรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc083-166">Pick order template</span></span>

1. <span data-ttu-id="fc083-167">เลือกกำหนดเท็มเพลตโดยใช้ตัวแก้ไขข้อความหรือ HTML</span><span class="sxs-lookup"><span data-stu-id="fc083-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="fc083-168">ดูรายการ [โทเค็นที่สนับสนุน](#supported-tokens-in-the-email-template) ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="fc083-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="fc083-169">ลงชื่อเข้าใช้ Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="fc083-170">ใช้เมนูด้านซ้าย ไปที่ **โมดูล \> การจัดการองค์กร \> ตั้งค่า \> เท็มเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="fc083-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="fc083-171">ขยายรายการด้านซ้ายเพื่อดูเท็มเพลตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fc083-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="fc083-172">สำหรับแต่ละเท็มเพลตที่คุณต้องการกำหนดเอง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="fc083-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="fc083-173">เลือกเท็มเพลตในรายการ</span><span class="sxs-lookup"><span data-stu-id="fc083-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="fc083-174">ภายใต้ **เนื้อหาของข้อความอีเมล** ให้เลือกรุ่นภาษาที่เหมาะสมในรายการ</span><span class="sxs-lookup"><span data-stu-id="fc083-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="fc083-175">(ภาษาเริ่มต้นคือ **en-us**)</span><span class="sxs-lookup"><span data-stu-id="fc083-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="fc083-176">ใต้ **เนื้อหาข้อความอีเมล** ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="fc083-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="fc083-177">บานหน้าต่าง **อัปโหลดเท็มเพลตอีเมล** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="fc083-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="fc083-178">เลือก **เรียกดู** และค้นหาไฟล์ HTML ที่มีเนื้อหาที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fc083-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="fc083-179">เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="fc083-179">Select **Upload**.</span></span> <span data-ttu-id="fc083-180">เท็มเพลตของคุณจะถูกอัปโหลดไปยังระบบ และตัวอย่างจะแสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="fc083-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="fc083-181">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fc083-181">Select **OK**.</span></span>
    1. <span data-ttu-id="fc083-182">ไม่จำเป็น: กำหนดคุณสมบัติ **ชื่อเรื่อง** ของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="fc083-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="fc083-183">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fc083-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="fc083-184">โทเคนที่สนับสนุนในเท็มเพลตอีเมล์</span><span class="sxs-lookup"><span data-stu-id="fc083-184">Supported tokens in the email template</span></span>

<span data-ttu-id="fc083-185">เมื่ออีเมลถูกส่ง โทเคนเหล่านี้จะถูกแทนที่ด้วยค่าจริงที่ใช้กับลูกค้าและใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc083-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="fc083-186">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="fc083-186">Sales order</span></span>

<span data-ttu-id="fc083-187">โทเคนต่อไปนี้จะใช้กับใบสั่งขายในภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fc083-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="fc083-188">ชื่อของโทเคน</span><span class="sxs-lookup"><span data-stu-id="fc083-188">Name of the token</span></span> | <span data-ttu-id="fc083-189">โทเคน</span><span class="sxs-lookup"><span data-stu-id="fc083-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="fc083-190">หมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-190">Order number</span></span>      | <span data-ttu-id="fc083-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="fc083-191">%salesid%</span></span> |
| <span data-ttu-id="fc083-192">ชื่อของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="fc083-192">Customer's name</span></span>   | <span data-ttu-id="fc083-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="fc083-193">%customername%</span></span> |
| <span data-ttu-id="fc083-194">ที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-194">Delivery address</span></span>  | <span data-ttu-id="fc083-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="fc083-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="fc083-196">ที่อยู่ที่เรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="fc083-196">Billing address</span></span>   | <span data-ttu-id="fc083-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="fc083-197">%customeraddress%</span></span> |
| <span data-ttu-id="fc083-198">วันที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-198">Order date</span></span>        | <span data-ttu-id="fc083-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="fc083-199">%shipdate%</span></span> |
| <span data-ttu-id="fc083-200">วิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-200">Delivery mode</span></span>     | <span data-ttu-id="fc083-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="fc083-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="fc083-202">ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="fc083-202">Discount</span></span>          | <span data-ttu-id="fc083-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="fc083-203">%discount%</span></span> |
| <span data-ttu-id="fc083-204">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="fc083-204">Sales tax</span></span>         | <span data-ttu-id="fc083-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="fc083-205">%tax%</span></span> |
| <span data-ttu-id="fc083-206">ผลรวมของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-206">Order total</span></span>       | <span data-ttu-id="fc083-207">%total%</span><span class="sxs-lookup"><span data-stu-id="fc083-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="fc083-208">รายการขาย</span><span class="sxs-lookup"><span data-stu-id="fc083-208">Sales line</span></span>

<span data-ttu-id="fc083-209">โทเคนต่อไปนี้จะถูกแทนที่ด้วยค่าสำหรับผลิตภัณฑ์แต่ละรายการในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="fc083-210">วางโทเค็น **รายการผลิตภัณฑ์ - เริ่มต้น** ที่จุดเริ่มต้นของบล็อก HTML ที่ถูกทำซ้ำสำหรับทุกผลิตภัณฑ์ และวางโทเค็น **รายการผลิตภัณฑ์ - สิ้นสุด** ที่ส่วนท้ายของบล็อก</span><span class="sxs-lookup"><span data-stu-id="fc083-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="fc083-211">ชื่อของโทเคน</span><span class="sxs-lookup"><span data-stu-id="fc083-211">Name of the token</span></span>      | <span data-ttu-id="fc083-212">โทเคน</span><span class="sxs-lookup"><span data-stu-id="fc083-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="fc083-213">รายการผลิตภัณฑ์ - เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fc083-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="fc083-214">รายการผลิตภัณฑ์ - สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="fc083-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="fc083-215">ชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fc083-215">Product name</span></span>           | <span data-ttu-id="fc083-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="fc083-216">%lineproductname%</span></span> |
| <span data-ttu-id="fc083-217">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="fc083-217">Description</span></span>            | <span data-ttu-id="fc083-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="fc083-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="fc083-219">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="fc083-219">Quantity</span></span>               | <span data-ttu-id="fc083-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="fc083-220">%linequantity%</span></span> |
| <span data-ttu-id="fc083-221">ราคาต่อหน่วยในรายการ</span><span class="sxs-lookup"><span data-stu-id="fc083-221">Line unit price</span></span>        | <span data-ttu-id="fc083-222">%lineprice% (ตรวจสอบ)</span><span class="sxs-lookup"><span data-stu-id="fc083-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="fc083-223">จำนวนสินค้าทั้งหมดในรายการ</span><span class="sxs-lookup"><span data-stu-id="fc083-223">line item total</span></span>        | <span data-ttu-id="fc083-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="fc083-224">%linenetamount%</span></span> |
| <span data-ttu-id="fc083-225">line discount / ส่วนลดต่อรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc083-225">line discount</span></span>          | <span data-ttu-id="fc083-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="fc083-226">%linediscount%</span></span> |
| <span data-ttu-id="fc083-227">วันที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-227">Ship date</span></span>              | <span data-ttu-id="fc083-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="fc083-228">%lineshipdate%</span></span> |
| <span data-ttu-id="fc083-229">วิธีการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="fc083-229">Procurement method</span></span>     | <span data-ttu-id="fc083-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="fc083-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="fc083-231">delivery address / ที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fc083-231">delivery address</span></span>       | <span data-ttu-id="fc083-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="fc083-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="fc083-233">หน่วยการขายของรายการ</span><span class="sxs-lookup"><span data-stu-id="fc083-233">Sales unit of the line</span></span> | <span data-ttu-id="fc083-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="fc083-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="fc083-235">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fc083-235">Additional resources</span></span>

[<span data-ttu-id="fc083-236">ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="fc083-237">เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="fc083-238">ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="fc083-239">ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="fc083-240">FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="fc083-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="fc083-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="fc083-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="fc083-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="fc083-243">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="fc083-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="fc083-244">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fc083-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]